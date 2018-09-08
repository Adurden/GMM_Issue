# GMM_Issue
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/Adurden/GMM_Issue/master)

### The purpose if this notebook is to illustrate a behaviour of the Gaussian Mixture from the sklearn library.

##### The data being used is from a greyscale video. When the GMM is trained with a warm start frame by frame with each frame's intermediates initializing the next frame's fit. However on some videos, components of the mixture are collapsed to a mean of (0,0) with a diagonal covariance matrix near zero.

##### In this notebook we will hard load in the Gaussian Parameters from frame 33, the last frame without any collapsed components, and use them to initialize a new GMM and fit it to frame 44, the first frame to have collapsed components. This is to manually recreate the deterministic fitting process executed by a repetitive fitting process with the warm start option enabled.
