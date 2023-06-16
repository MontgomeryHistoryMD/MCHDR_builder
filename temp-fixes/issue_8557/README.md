# Temporary Fix to DSpace Issue 8557

There is a partially resolved bug in DSpace 6 in which the handle server
from org.dspace does not start.

A description of the problem and the proposed temporary fix is found
at [DSpace:DSpace Issue 8557](https://github.com/DSpace/DSpace/issues/8557).

The fix that we are using is to replace handle-6.2.jar from the DSpace
with handle.jar file from [CNRI](https://www.handle.net/hs-source/hdl6.2.5_03.tar.gz)
in the build script, after the package is built for the first time. Maven is
run again in order to build the .war files with the replaced file.

The .jar file is in this directory, and the fix is in the build script.
