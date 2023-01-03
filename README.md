# LunaLogger
> Basic logger that writes log messages to both the console and a text file

# LunaLogger Class

The `LunaLogger` class provides a simple way to output log messages to the console and a text file. It has a single `log` function that takes a log level, file name, line number, and message as arguments, and it outputs the log message to the console and the text file with a timestamp and the log level. The console text color is set based on the log level:

* Info: White
* Warning: Yellow
* Error: Red

## Dependencies

The `LunaLogger` class requires the following headers:

* `<Windows.h>`: Provides access to the `SetConsoleTextAttribute` function, which is used to set the console text color.
* `<sstream>`: Provides the `std::stringstream` class, which is used to format the timestamp for the log messages.
* `<ctime>`: Provides the `std::time` and `std::localtime_s` functions, which are used to get the current time.
* `<iomanip>`: Provides the `std::put_time` function, which is used to format the timestamp for the log messages.
* `<fstream>`: Provides the `std::ofstream` class, which is used to write the log messages to a text file.

## Usage

To use the `LunaLogger` class, you can simply call the `log` function and pass it the log level and message you want to output, like this:

```cpp
LunaLogger::log(LogLevel::Info, FILE, LINE, "This is an info log message");
LunaLogger::log(LogLevel::Warning, FILE, LINE, "This is a warning log message");
LunaLogger::log(LogLevel::Error, FILE, LINE, "This is an error log message");
```
