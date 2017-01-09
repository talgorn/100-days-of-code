# 100 Days Of Code - Log
**Link to work:** [Living theater](https://github.com/talgorn/100-days-of-code.git)


Day 0: January 4, 2017
**Today's Progress**: Created and updated Git repo,  added a project Overview to the README.MD, tried for an hour to make Camera functions properly. I either had a blank screen when working with Android docs, or a halt at launch time with an example project. So far , so almost_good :)
**Thoughts:** Not the first time Android Dev docs provide biased infos.


Day 1: January 5, 2017
**Today's Progress**: 
Struggled again with Camera camera for an hour. Eventually found a straightforward working example for computer vision (Link 3).
Will definitely work with OpenCV for android for object tracking. Maybe for Camera management. Will depend on OpenGL integration (TBD).
Installed and configured OpenCV for android in Android Studio. Almost done.
I spent something like 1h30  on the project today.
**Thoughts**:
Video stream and object tracking are beaten paths, quite well documented.
The reconstruction of objects' parts masked by fingers will be the true challenge of course.


Day 2: January 6, 2017
**Today's Progress**: 
Still had issues with OpenCV for android & Android studio configuration.
Played around (C++) with OpenCV for OSX / Xcode to get hands dirty with object tracking.
I spent something like 2h30  on the project today.
**Thoughts**:
OpenCV seems a great API. SO easy to get started.
Had an idea to avoid the reconstruction part.  The whole process would be:
1) Set stage (Save fixed bacground)
2) Enroll Actors = For each actor, put it anywhere on the stage -> Extract Object  -> Define histogram / shape for each of them
3) Take = Start recording the scene
4) Magic = Track position and orientation of actors -> For each frame: draw background then rotate and draw actors
5) If tracking fast enough, magic can occur in real time. 

Day 3: January 7, 2017
**Today's Progress**: 
Experiments (and had fun) with object extraction with openCV.
I spent something like 3h30  on the project today.
**Thoughts**:
Basic feature extractions methods (greyscale subs and absDiff based) are not good enough for the project.
Will refine the approach (per channel diff) and give a try to others techniques (like templates).
As usual, will have to find the good compromise between performance and speed .

Day 4: January 8, 2017
**Today's Progress**: 
Got a first rough object extraction by calculating delta of pixel intensity between two greyscaled images
(fixed background and live feed) . I used a treshold to select background/added object on the scene.
I spent something like 3h00  on the project today.
**Thoughts**:
I will need to spend some time on literature to select a feature extraction that match the needs of this project.
Many candidates. Will have to trade between speed/performance.

Day 5: January 9, 2017
**Today's Progress**: 
No code today but researched best solutions for the project.
The winners are:
BackgroundSubtractorMOG2 for background extraction (actor extraction);
BRIEF keypoints descriptors;
STAR feature detection (OpenCV's Censure implementation).
I spent something like 1H30 on the project today.
**Thoughts**:
I will need to spend some time now to test / experiment with the implementation on OSX.
These techniques can be used on mobile platformthe but I don't know what it would give on good enough smartphones/tablet.


**Link(s) to work**:
1. [Alternate android projects](https://github.com/commonsguy/cw-advandroid/tree/master/Camera). 
2. [Official android docs](https://developer.android.com/guide/topics/media/camera.html)
3. [Helloworld for computer vision](http://www.hasper.info/hello-world-for-android-computer-vision/)
4. [OpenCV tracking demo project](https://www.youtube.com/watch?annotation_id=annotation_307976421&feature=iv&src_vid=RS_uQGOQIdg&v=bSeFrPrqZ2A)
