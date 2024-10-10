This repository contains ready-to-use python wheels to install opencv-python in a headless environment such as AWS Lambda. The wheels support the x264/x265 codecs so that you can save video files in opencv with h264/h265 encoding. This is extremely useful if you want to produce files that are playable on a web browser.

On an AWS Lambda environment, you can install and use these wheels as added layers to your Lambda function or, alternatively, using the EFS (Elastic File System) service.

When using opencv-python in your function, to write a video file with h264 encoding, use the following function:

vid = cv2.VideoWriter('video.mp4', cv2.VideoWriter_fourcc(*'avc1'), fps, (width, height))

If you are using these wheels and you find them useful, please consider making a donation of 20 GBP/EUR/USD to https://paypal.me/uropanet

I have spent several days understanding how to put all the pieces together using Docker and compiling various libraries as well as FFmpeg.

The wheels are distributed as they are with no specific licence attached to them. However, given the differences in licences between ffmpeg and x264/x265, you should be aware of what you can and can't do commercially or in redistributing them.

