
sudo apt-get install libmosquitto-dev  
install the above libmosquitto-dev on ubuntu before compliation of mosquitto client.  it provide the mosquitto.h head file and library to support mosquitto function call

g++ -o mqtt_json_publisher mqtt_json_publisher.cpp -lmosquitto -I./rapidjson

g++ -o mqtt_publisher mqtt_publisher.cpp -lmosquitto -I./rapidjson

g++ -o mqtt_subscriber mqtt_subscriber.cpp -lmosquitto -I./rapidjson

g++ -o mqtt_json_config_publisher mqtt_json_config_publisher.cpp -lmosquitto -I./rapidjson -lconfig++

 execute the subscriber and publisher in seperate terminal.
 publisher read the data.json file and push the data on the topic ( test ) on mosquito server.
