DMLogFormatter a CocoaLumberjack Log Formatter
==============================================

We are using the `DMLogFormatter` in our projects to clean up the console output. Feel free to use it in your project. It should be used with the [CocoaLumberjack](https://github.com/robbiehanson/CocoaLumberjack) framework.

##Usage

Like this:

    #import "DMLogFormatter.h"

    - (void)initLogger
    {
        DDTTYLogger *ttyLogger = [DDTTYLogger sharedInstance];
        ttyLogger.logFormatter = [[DMLogFormatter alloc] init];
        [DDLog addLogger:ttyLogger];
    }

##Sample Output

<table width="100%">
  <tr>
    <th>Level</th>
    <th>Date</th>
    <th>@ Caller</th>
    <th>(Line Number)</th>
    <th># Message</th>
  </tr>
</table>

            05.10.2012 16:10:41:622 @ AppDelegate.application:didFinishLaunchingWithOptions: (24) # This is a verbose message.
            05.10.2012 16:10:41:622 @ AppDelegate.application:didFinishLaunchingWithOptions: (25) # This is a info message.
    WARNING 05.10.2012 16:10:41:622 @ AppDelegate.application:didFinishLaunchingWithOptions: (26) # This is a warn message.
      ERROR 05.10.2012 16:10:41:622 @ AppDelegate.application:didFinishLaunchingWithOptions: (27) # This is a error message.

##License

Under MIT Licence.

---

Your devmob team.