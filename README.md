Sonar Findbugs 
==========

## Description / Features
This plugin requires the (Java Plugin)[http://docs.sonarqube.org/display/PLUG/Java+Plugin], and uses (FindBugs)[http://findbugs.sourceforge.net/], (fb-contrib)[http://fb-contrib.sourceforge.net/] and (Find Security Bugs)[http://h3xstream.github.io/find-sec-bugs/] to provide coding rules.

Since version 3.0, the plugin embed FindBugs 3.0.0 which supports analysis of Java 8 bytecode but requires Java 1.7 to run (see Compatibility section)

A majority of the FindBugs rules have been rewritten in the Java plugin. Rewritten rules are marked "Deprecated" in the FindBugs plugin, but a (concise summary of replaced rules)[http://dist.sonarsource.com/reports/coverage/findbugs.html] is available.

## Usage
In the quality profile, activate some rules from the FindBugs, fb-contrib or FindSecBugs rule repositories and run an analysis on your project.

### Compiled code
FindBugs requires the compiled classes to run.

Make sure that you compile your source code with debug information on (to get the line numbers in the Java bytecode). Debug is usually on by default unless you're compiling with Ant, in which case, you will need to turn it on explicitly. If the debug information is not available, the issues raised by FindBugs will be displayed at the beginning of the file because the correct line numbers were not available.


## Compatibility 
Version 3.0.0 of findbugs requires java 1.7 to run. Please find below the compatibility matrix of the plugin.

Findbugs Plugin version|Embedded Findbugs version|Embedded Findsecbugs version|Embedded FB-Contrib version|Minimal Java version
---|---|---|---|---
2.4|2.0.3|N/A|5.2.1|1.6
3.0|3.0.0|N/A|6.0.0|1.7
3.2|3.0.1|1.3.0|6.0.0|1.7
3.3|3.0.1|1.4.2|6.2.3|1.7
