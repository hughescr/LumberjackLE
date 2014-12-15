Lumberjack logger for LogEntries
================================

HOWTO
-----

1. Follow instructions for https://github.com/CocoaLumberjack/CocoaLumberjack
2. Add the lelib from https://github.com/logentries/le_ios
3. You do not need to interact with lelib directly yourself, so don't put their initialization code in you app, probably.
4. Add these files here to your project
5. #import "LogEntriesLogger.h"
6. Do this, probably in -application:didFinishLaunchingWithOptions:

```Objective-C
    LogEntriesLogger *logEntriesLogger = [[LogEntriesLogger alloc] initWithLogEntriesToken:@"your-logentries-token-here"];
    logEntriesLogger.logFormatter = [[HelpfulInfoLogFormatter alloc] init];
    [DDLog addLogger:logEntriesLogger];
```
