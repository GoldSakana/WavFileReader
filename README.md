# WavFileReader
Simple WAV file reader(loader) in C++.

Create WavFileReader object and use WavFileReader.Read() function to read data from WAV file.  
The way of using it is very similar to fread() function in stdio.h or cstdio.  
See example/sample.cpp for more details.

## Notice
* Supported WAV format are 8bit and 16bit.
* WavFileReader.Read() function has several overloads that accept different data types. Convenient isn't it?
* Loaded data will be automatically converted and downsized from signed 16bit to unsigned 8bit by WavFileReader.Read() function ONLY when the WAV format is 16bit and prepared buffer is 8bit.
* WavFileReader() constructor throws WFRException object defined in wav_file_reader.h when some exception occured.
* Second arg of WavFileReader.Read() function is not a size of buffer but a count of elements in buffer.
* WavFileReader.Read() function returns (the total number of samples successfully read)/(NumChannels).
* WavFileReader.Seek() function returns the same value as fseek() function in stdio.h or cstdio.
