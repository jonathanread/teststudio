---
title: Video Recording for a Test List
page_title: Video Recording for a Test List
description: "Test Studio Test List Execution. How to run a test list in Test Studio. Automatic re-run rerun of failed test in a test list. recording options for test list execution in Test Studio"
position: 3
---
# How Video Recording of a Test List Helps

Test Studio provides a rich set of <a href="/features/test-lists/test-list-settings" target="_blank">test list settings</a> to help for stable execution of the test suites and easier debugging in case of failures.

Test lists are designed for unattended execution and as such, you cannot always observe the test list run. Sometimes there are test list failures, specific for a particular machine, or time of execution, etc., which is difficult to reproduce and debug.

## Enable Screen Recording for Test List Execution

Observing the test list execution in such occasions, usually turns out to be helpful to understand what caused the failure. Therefore Test Studio provides built-in settings for capturing a video of the test list execution. __By default the screen recording option is disabled__, but you can choose between _always enabled_ or _enable only on failure_.

![Screen recording Settings][4]

## Watch the Video from the Test List Execution

The <a href="/automated-tests/test-list-results/analyze-test-list-results#test-list-screen-recording-results" target="_blank">results</a> for a test list, which captures a video of the execution, contain a specific _'Screen Recording Info'_ icon to provide access to the video.

## Recording Settings Specifics

Below are listed the settings related to screen recording of test list execution with the specifics related to each one.

* __Recording Codec__
   
Supported codecs are:
   - Motion JPEG (Biggest file size)

   - X264: [x264 download page](https://sourceforge.net/projects/x264vfw/)

   - Xvid: [Xvid download page](https://www.xvid.com/download/)
   
After installing XVID, _"Display encoder status"_ encoder setting must be disabled. From Windows Start menu open _"Encoder Config"_ ->

![Windows Start Menu][1]

Click _"Other Options.."_ -> Uncheck _"Display encoder status"_

![XVID config][2]

> The default selected codec __MJPEG__ can be used without any further adjustments. <br/> 
> In order to use __Xvid or X264__ codecs, they must be installed on the execution machine (for local and Visual Studio runs on the local machine, and for remote runs, on the machine where test list will be executed)

* __Recording FPS__ - Sets captured video frames per second. Lower number produces smaller files.

* __Recording mode__ - Sets recording mode. There are three different recording modes:
    - Off (Default) - In this mode no video recordings are created.

    - Always - Video recordings for all executed tests are saved.

    - OnFail - Only video recordings for failed tests are saved.

* __Recording output location__ - Sets path to output location for all video files. If no value is set, for local test list runs default location is project results folder. __Always set location for remote or Visual Studio runs.__
   
> For remote executions best practice is to use a shared folder accessable from all remote execution agents. <br/>

* __Recording scale__ - Sets downscaling of the recorded video in percents. From 10 to 100 <br/>

	- _Example:_ If set to 100 the original screen resolution is preserved. When the scale is set to 50 % the resolution of video is halved.
   
> Lower number produces smaller files, but decreases video quality.

*  __Recording size limit__ - Sets file size limit in megabytes, 0 is unlimited size. 

> If the limit is reached, video recording will be stopped before the test execution ends.

[1]: /img/automated-tests/test-lists/test-list-runs-specifics/fig1.png
[2]: /img/automated-tests/test-lists/test-list-runs-specifics/fig2.png
[3]: /img/automated-tests/test-lists/test-list-runs-specifics/fig3.png
[4]: /img/automated-tests/test-lists/test-list-runs-specifics/fig4.png
