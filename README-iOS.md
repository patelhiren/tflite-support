# Building framework for iOS

Install Bazel using Bazelisk

See: <https://bazel.build/install/bazelisk>

Install `conda` and `tensorflow` environment.

```console
conda create -n tensorflow python=3.9
```

Activate the conda activate tensorflow environment

```console
conda activate tensorflow
conda install -c apple tensorflow-deps
```

Build using the command:

```console
bazel build -c opt --config=ios_arm64 //tensorflow_lite_support/ios:TensorFlowLiteTaskVision_framework
```

Output path will be logged in terminal.

```console
Target //tensorflow_lite_support/ios:TensorFlowLiteTaskVision_framework up-to-date:
  bazel-out/applebin_ios-ios_arm64-opt-ST-2967bd56a867/bin/tensorflow_lite_support/ios/TensorFlowLiteTaskVision_framework.zip
```

The zip file has the compressed .framework to use.
