
sudo apt-get install libmosquitto-dev  
install the above libmosquitto-dev on ubuntu before compliation of mosquitto client.  it provide the mosquitto.h head file and library to support mosquitto function call

RapidJSON
Download RapidJSON: You can download the RapidJSON header files directly from its GitHub repository: https://github.com/Tencent/rapidjson. You can either clone the repository or download the header files directly.
Include RapidJSON in Your Project: Once you have the RapidJSON header files, simply include them in your C++ source files where you need to use them:
#include "rapidjson/document.h"
Compilation: When compiling your program, make sure to include the directory containing the RapidJSON header files in the include path. You can do this using the -
Since RapidJSON is a header-only library, you don't need to perform any installation steps beyond obtaining the header files and ensuring that they are included in your compilation process.

sudo apt-get install libconfig++-dev 
install libconfig for configuration

g++ -o mqtt_json_publisher mqtt_json_publisher.cpp -lmosquitto -I./rapidjson
g++ -o mqtt_publisher mqtt_publisher.cpp -lmosquitto -I./rapidjson
g++ -o mqtt_subscriber mqtt_subscriber.cpp -lmosquitto -I./rapidjson
g++ -o mqtt_json_config_publisher mqtt_json_config_publisher.cpp -lmosquitto -I./rapidjson -lconfig++

 execute the subscriber and publisher in seperate terminal.
 publisher read the data.json file and push the data on the topic ( test ) on mosquito server.
