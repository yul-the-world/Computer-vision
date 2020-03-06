# Computer_vision

This is the source code that summarizes the codes that I have gathered while attending Professor Sungho Kim's class (Yeungnam University, computer vision class) and my personal studies.

**1.  Install OpenCV**
--
- I installed [OpenCV version(2.4.13.6)](https://opencv.org/releases/)
- Environment variables: C:\opencv24136\build\x86\vc14\bin;
- VS Setting
    - Include Directories
         - C:\OpenCV24136\build\Include
    - Library Directories
         - C:\opencv24136\build\x86\vc14\lib
    - Additional Dependencies
         - opencv_calib3d2413d.lib;
opencv_contrib2413d.lib;
opencv_core2413d.lib;
opencv_features2d2413d.lib;
opencv_flann2413d.lib;
opencv_gpu2413d.lib;
opencv_highgui2413d.lib;
opencv_imgproc2413d.lib;
opencv_legacy2413d.lib;
opencv_ml2413d.lib;
opencv_nonfree2413d.lib;
opencv_objdetect2413d.lib;
opencv_ocl2413d.lib;
opencv_photo2413d.lib;
opencv_stitching2413d.lib;
opencv_superres2413d.lib;
opencv_ts2413d.lib;
opencv_video2413d.lib;
opencv_videostab2413d.lib;



**2. Camera Distortion**
--

- Result

|INPUT|OUTPUT|
|------|---|
|![soccer_distortion](https://user-images.githubusercontent.com/56310078/76083123-34bfdb80-5ff0-11ea-9796-43c0a911ceac.JPG)|![2_camera_distortion_result](https://user-images.githubusercontent.com/56310078/76083138-3a1d2600-5ff0-11ea-9433-7b1abac7e9c6.jpg)|

**3. Color Space**
--

- Result

|INPUT|OUTPUT(Blue)|OUTPUT(Green)|OUTPUT(Red)|
|------|---|---|---|
|![corni_fructus](https://user-images.githubusercontent.com/56310078/76083276-92ecbe80-5ff0-11ea-8aef-60ea1ed2a52c.jpg)|![3_color_blue](https://user-images.githubusercontent.com/56310078/76083261-89fbed00-5ff0-11ea-8c9f-0ee4d846f4d7.jpg)|![3_color_green](https://user-images.githubusercontent.com/56310078/76083263-8b2d1a00-5ff0-11ea-8706-a884edb95961.jpg)|![3_color_red](https://user-images.githubusercontent.com/56310078/76083266-8cf6dd80-5ff0-11ea-8b5e-df3049b0cc12.jpg)|

- Another result

|INPUT|OUTPUT(Blue)|OUTPUT(Green)|OUTPUT(Red)|
|------|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76084072-718cd200-5ff2-11ea-98cd-8b92390aea6a.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084158-9bde8f80-5ff2-11ea-815f-0a85ca2403bb.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084154-9aad6280-5ff2-11ea-800c-e2061737eb9c.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084152-997c3580-5ff2-11ea-957d-aa1a98f2e491.jpg" width="150" height="150">|

- Input color

|INPUT|OUTPUT(Blue)|OUTPUT(Green)|OUTPUT(Red)|
|------|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76084072-718cd200-5ff2-11ea-98cd-8b92390aea6a.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084514-5cfd0980-5ff3-11ea-998d-8f1f670e204c.png" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084510-5bcbdc80-5ff3-11ea-9e21-df6b9b88bbf3.png" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76084508-5b334600-5ff3-11ea-87be-4d03309f7a99.png" width="150" height="150">|

- Builtin function vs Implementation (RGB to Gray)

|INPUT|OUTPUT(Builtin)|OUTPUT(Implementation)|
|------|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76084072-718cd200-5ff2-11ea-98cd-8b92390aea6a.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085021-8cf8dc80-5ff4-11ea-809e-fc485a5e0b13.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085028-8e2a0980-5ff4-11ea-9498-d9712e9057e9.jpg" width="200" height="200">|

- Builtin function vs Implementation (RGB to HSI)

|INPUT|OUTPUT(Builtin-HSV)|OUTPUT(Implementation-HSI)|
|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76084072-718cd200-5ff2-11ea-98cd-8b92390aea6a.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085641-cc73f880-5ff5-11ea-9b2b-a8f3ff258cff.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085643-cda52580-5ff5-11ea-805c-bf5fe749549a.jpg" width="200" height="200">|

- HSI(Hue, Saturation, Intensity) of Implementation

|Hue|Saturation|Intensity|
|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76085648-ced65280-5ff5-11ea-8844-9f5ed2b783f7.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085649-d0077f80-5ff5-11ea-9dfa-1fd499205b3d.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085653-d1d14300-5ff5-11ea-9c1b-8adfb4fb283b.jpg" width="200" height="200">|

- Builtin function vs Implementation (RGB to HSV)

|INPUT|OUTPUT(Builtin-HSV)|OUTPUT(Implementation-HSV)|
|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76084072-718cd200-5ff2-11ea-98cd-8b92390aea6a.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76085641-cc73f880-5ff5-11ea-9b2b-a8f3ff258cff.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76090098-4d36f280-5ffe-11ea-8a92-a61d428e682a.jpg" width="200" height="200">|

- HSV(Hue, Saturation, Value) of Implementation

|Hue|Saturation|Value|
|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76090099-4dcf8900-5ffe-11ea-8440-e5c01638803f.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76090103-4f00b600-5ffe-11ea-9c7b-adc461fc66ef.jpg" width="200" height="200">|<img src="https://user-images.githubusercontent.com/56310078/76090104-5031e300-5ffe-11ea-9a5e-15bb1915c41e.jpg" width="200" height="200">|

**4. Image Filtering**
--

- Blur Result(Smoothed Image)

|INPUT|OUTPUT(Kernel 1X1)|OUTPUT(Kernel 3X3)|OUTPUT(Kernel 5X5)|
|------|---|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76087010-a56af600-5ff8-11ea-8817-9f2f09786918.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087030-ae5bc780-5ff8-11ea-8a91-f8ee28d74448.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087032-aef45e00-5ff8-11ea-9d2d-a7a82587b9b9.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087033-b0258b00-5ff8-11ea-9d17-a4fd3d094acd.jpg" width="150" height="150">|
|OUTPUT(Kernel 11X11)|OUTPUT(Kernel 19X19)|OUTPUT(Kernel 25X25)|OUTPUT(Kernel 29X29)|
|<img src="https://user-images.githubusercontent.com/56310078/76087054-b582d580-5ff8-11ea-82d9-9dfe15ac3667.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087057-b7e52f80-5ff8-11ea-9227-d35d6239d454.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087063-bae02000-5ff8-11ea-824b-b35839d9a86e.jpg" width="150" height="150">|<img src="https://user-images.githubusercontent.com/56310078/76087073-bddb1080-5ff8-11ea-80ac-a4f2ef0bd19b.jpg" width="150" height="150">|

- Salt & Pepper Result(Filtered Image Median vs Gaussian)

|INPUT|OUTPUT(Salt&Pepper Noised)|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76087010-a56af600-5ff8-11ea-8817-9f2f09786918.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76087513-a5b7c100-5ff9-11ea-8baa-a7b3ff27ca0d.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 1X1)|OUTPUT(Gaussian Filtered 1X1)|
|<img src="https://user-images.githubusercontent.com/56310078/76088019-a866e600-5ffa-11ea-9f67-ec1d50d24bad.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76087994-9e44e780-5ffa-11ea-95b1-3e4327836b82.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 3X3)|OUTPUT(Gaussian Filtered 3X3)|
|<img src="https://user-images.githubusercontent.com/56310078/76088022-a9981300-5ffa-11ea-9b17-ef56a9f42179.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76087996-9f761480-5ffa-11ea-9a1f-f8a48aa4ded1.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 5X5)|OUTPUT(Gaussian Filtered 5X5)|
|<img src="https://user-images.githubusercontent.com/56310078/76088026-aac94000-5ffa-11ea-9ef0-a4558ff3551f.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088000-a00eab00-5ffa-11ea-83a5-6482c657e488.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 7X7)|OUTPUT(Gaussian Filtered 7X7)|
|<img src="https://user-images.githubusercontent.com/56310078/76088030-abfa6d00-5ffa-11ea-9140-4676a85bce24.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088004-a1d86e80-5ffa-11ea-9081-5ff3e7397004.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 9X9)|OUTPUT(Gaussian Filtered 9X9)|
|<img src="https://user-images.githubusercontent.com/56310078/76088034-ad2b9a00-5ffa-11ea-9f2a-0f48d104fbd8.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088008-a3a23200-5ffa-11ea-8831-3786e2c9e1de.jpg" width="400" height="400">|

- Salt & Pepper Result(Filtered Image Sigma of Gaussian)

|OUTPUT(sigmaX, sigmaY = 1)|OUTPUT(sigmaX, sigmaY = 3)|OUTPUT(sigmaX, sigmaY = 5)|
|------|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76088415-5d999e00-5ffb-11ea-8fd4-eb671fb59f81.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76088419-5ffbf800-5ffb-11ea-8620-d00012e82785.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76088427-612d2500-5ffb-11ea-91a9-51cd4bd04892.jpg" width="300" height="300">|

- Gaussian Noised Result(Filtered Image Median vs Gaussian)

|Gaussian Noise|Gaussian Kernel example|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76088890-24156280-5ffc-11ea-8792-27e5984a5048.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088894-25df2600-5ffc-11ea-9b51-aed02a0a9576.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 1X1)|OUTPUT(Gaussian Filtered 1X1)|

|INPUT|OUTPUT(Gaussian Noised)|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76087010-a56af600-5ff8-11ea-8817-9f2f09786918.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088942-3b545000-5ffc-11ea-861e-e6832170715c.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 1X1)|OUTPUT(Gaussian Filtered 1X1)|
|<img src="https://user-images.githubusercontent.com/56310078/76088992-4c04c600-5ffc-11ea-908e-456ed09699d0.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088949-3c857d00-5ffc-11ea-84bc-6e053ebea2dd.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 3X3)|OUTPUT(Gaussian Filtered 3X3)|
|<img src="https://user-images.githubusercontent.com/56310078/76088998-4d35f300-5ffc-11ea-88f2-a4a1afe50470.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088954-3db6aa00-5ffc-11ea-8cec-42c387fa7956.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 5X5)|OUTPUT(Gaussian Filtered 5X5)|
|<img src="https://user-images.githubusercontent.com/56310078/76089001-4dce8980-5ffc-11ea-9a01-3c3d37d4b990.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088963-3f806d80-5ffc-11ea-8d41-42b53a57983f.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 7X7)|OUTPUT(Gaussian Filtered 7X7)|
|<img src="https://user-images.githubusercontent.com/56310078/76089005-4effb680-5ffc-11ea-9435-c44b37bc9bff.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088969-414a3100-5ffc-11ea-8f09-089022fc0853.jpg" width="400" height="400">|
|OUTPUT(Median Filtered 9X9)|OUTPUT(Gaussian Filtered 9X9)|
|<img src="https://user-images.githubusercontent.com/56310078/76089009-5030e380-5ffc-11ea-9cb1-11f9355881fc.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76088972-427b5e00-5ffc-11ea-8c89-3b7082f75a79.jpg" width="400" height="400">|

- Gaussian Noised Result(Filtered Image Sigma of Gaussian)

|OUTPUT(sigmaX, sigmaY = 1)|OUTPUT(sigmaX, sigmaY = 3)|OUTPUT(sigmaX, sigmaY = 5)|
|------|---|---|
|<img src="https://user-images.githubusercontent.com/56310078/76089336-ccc3c200-5ffc-11ea-9bca-f7442932085d.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76089338-cdf4ef00-5ffc-11ea-8df3-cb5f51213ad2.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76089340-cf261c00-5ffc-11ea-9b8d-e3fa70bd93db.jpg" width="300" height="300">|

**5. Edge**
--

- Canny edge

|INPUT|OUTPUT|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76087010-a56af600-5ff8-11ea-8817-9f2f09786918.jpg" width="400" height="400">|<img src="https://user-images.githubusercontent.com/56310078/76089630-5d9a9d80-5ffd-11ea-806d-2667db63520a.jpg" width="400" height="400">|

- Canny edge another Result

|INPUT|OUTPUT(Min Threshold0)|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76090314-af8ff300-5ffe-11ea-9f51-ad4bde899e3f.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76090542-16151100-5fff-11ea-914d-6b240743aae3.jpg" width="300" height="300">|
|OUTPUT(Min Threshold25)|OUTPUT(Min Threshold50)|
|<img src="https://user-images.githubusercontent.com/56310078/76090546-17463e00-5fff-11ea-9417-1a70101dbca7.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76090553-18776b00-5fff-11ea-8d93-ae519a310421.jpg" width="300" height="300">|
|OUTPUT(Min Threshold75)|OUTPUT(Min Threshold100)|
|<img src="https://user-images.githubusercontent.com/56310078/76090326-b4ed3d80-5ffe-11ea-901e-8132613ded14.jpg" width="400" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76090329-b61e6a80-5ffe-11ea-8d0c-6781fb114220.jpg" width="400" height="300">|

- Sobel edge

|X direction|Y direction|
|------|---|
|<img src="https://user-images.githubusercontent.com/56310078/76090886-c7b44200-5fff-11ea-89bf-ad210d498668.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76090889-c84cd880-5fff-11ea-9d38-31f36155a52c.jpg" width="300" height="300">|
|Magnitude(X+Y)|Direction(X,Y)|
|<img src="https://user-images.githubusercontent.com/56310078/76090893-caaf3280-5fff-11ea-9806-872624bba143.jpg" width="300" height="300">|<img src="https://user-images.githubusercontent.com/56310078/76090895-cc78f600-5fff-11ea-9ed3-792d2fa575e6.jpg" width="300" height="300">|
