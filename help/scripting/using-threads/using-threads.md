---
helpx_url: "https://helpx.adobe.com/kr/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: 병렬 처리 및 성능을 위해 Substance 3D Designer Python 스크립팅에서 스레드를 사용하는 방법을 알아봅니다.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 스레드 사용
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# 스레드 사용

플러그인이 Python 스레딩 관련 클래스에 대해 Python의 스레딩 모듈 *또는* Qt를 사용하여 <b>스레드를 생성</b>할 수 있습니다.

이 기능은 Designer이 실행되는 동안 백그라운드 처리 또는 I/O 작업을 수행하는 데 유용할 수 있습니다.

Designer의 Python API에 있는 대부분의 클래스와 메서드는 <b>기본 응용 프로그램 스레드</b>에서 *전용*&#x200B;으로 호출할 수 있습니다. 따라서 현재 Designer에 열려 있는 그래프를 수정하려면 기본 애플리케이션 스레드에서 해당 그래프를 수정해야 합니다.

가능한 한 가지 해결 방법은 다음 예제와 같이 <b>QThread</b> 및 <b>대기 중인 연결</b>을 사용하는 것입니다.

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
