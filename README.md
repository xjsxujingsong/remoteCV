
this is an example about how to use remote object detection based on openCV and zeromq framework.

<img src='https://raw2.github.com/funningboy/remoteCV/master/img/results.png'>

##requirements
- opencv(python) as cv(opencv) and cv2(numpy)
- zeromq(python)
- gevent(light weight switch)
- knowledge about img process
- profile, logging each stage mem and cpu time


##method
- Server
  - capture img
  - send img to clinet
  - wait for next command from client
  - update status by new command
- Client
  - receive img
  - run all detection
  - build up a new command based on detection results


##detections
- face detect
- circle detect
- line detect
- find attribute obj


##how to run it?
- python poll_camera.py (using cv to capture/show img via remote protocol)
- python poll_camera2.py (using cv2 to capture/show img ...)
- python poll_thread_run2.py (using cv2 to run all thread detection based on CPU num)
- python poll_series_run2.py (using cv2 to run all series detection ...)
