# phpmosquitto

<?php
// 连接到MQTT服务器
$mqtt = new Mosquitto\Client();
$mqtt->connect("localhost", 1883);

// 订阅主题
$topic = "test";
$mqtt->subscribe($topic, 0);

// 处理接收到的消息
$mqtt->onMessage(function ($message) {
    echo "Received message on topic {$message->topic}: {$message->payload}\n";
});

// 进行消息循环
while (true) {
    $mqtt->loop();
}

// 断开连接
$mqtt->disconnect();
?>
