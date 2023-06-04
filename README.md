# BaselineProfileApplication

**Application to test baseline profile library**

_Run the following command to generate the baseline-prof.txt file._

`./gradlew :app:generateReleaseBaselineProfile -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=BaselineProfile`

The generated file will be found under `build` package of `baselineprofile` module. 
Go to outputs then to `connected_android_test_additional_output` folder and look for the device used on tests.

_Run the following command to measusure the application startup metrics_

`./gradlew :baselineprofile:connectedAndroidTest -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=Macrobenchmark`


**Discoveries**

- We don't need macrobenchmark library import, just `baselineprofile` and `profileinstaller`.
- BaselineProfile needs his own module, like `macrobenchmark`.
- Using alpha versions of `baselineprofile` permits run baseline generating tasks without rooted physical devices.
- Maybe it's necessary upgrade gradle to 8.0.0 or above versions.
- BaselineProfile library already contains `macrobenchmark` jetpack library. The opposite is not valid.

**Results:**
![image](https://github.com/samuel8mille/BaselineProfileApplication/assets/13340536/f6167f71-8258-4692-95c6-347dd66522f0)



