# BaselineProfileApplication

**Application to test baseline profile library**

Run the following command to generate the baseline-prof.txt file.

`./gradlew :app:generateReleaseBaselineProfile -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=BaselineProfile`

The generated file will be found under `build` package of `baselineprofile` module. 
Go to outputs then to `connected_android_test_additional_output` folder and look for the device used on tests.

Run the following command to measusure the application startup metrics

`./gradlew :baselineprofile:connectedAndroidTest -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=Macrobenchmark`


**Results:**
![image](https://github.com/samuel8mille/BaselineProfileApplication/assets/13340536/f6167f71-8258-4692-95c6-347dd66522f0)



