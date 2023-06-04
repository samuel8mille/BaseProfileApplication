# BaselineProfileApplication

**Application to test baseline profile library**

Run the following command to generate the baseline-prof.txt file.

`./gradlew :app:generateReleaseBaselineProfile -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=BaselineProfile`

The generated file will be found under `build` package of `baselineprofile` module. 
Go to outputs then to `connected_android_test_additional_output` folder.

Run the following command to measusure the application startup metrics

`./gradlew :baselineprofile:connectedAndroidTest -Pandroid.testInstrumentationRunnerArguments.androidx.benchmark.enabledRules=Macrobenchmark`


**Results:**
![image](https://github.com/samuel8mille/BaselineProfileApplication/assets/13340536/2b626954-0464-4e29-b211-18739a5e38a3)


