# Introduction
Freeverb3 vst3 plugin using JUCE

# Build

```shell
# clone juce's source code, you can skip this if already had JUCE in your computer
git clone git@github.com:juce-framework/JUCE.git
cmake -DJUCE_SOURCE_DIR=/path/to/juce -S . -B build
cmake --build build
# then you can find a vst3 plugin in build/juce_plugin/Freeverb3_artefacts/Freeverb3.vst3
```