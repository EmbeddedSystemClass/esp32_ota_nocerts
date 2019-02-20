创建：sunhao 20190220

ESP32 OTA

取消certs验证

远程服务器开启http server指令

$python -m SimpleHTTPServer 8070


url = "http://39.98.160.32:8070/hello-world.bin"

  注释掉 esp_https_ota.c

    //sunhao
    /*if (!config->cert_pem) {
        ESP_LOGE(TAG, "Server certificate not found in esp_http_client config");
        return ESP_FAIL;
    }*/


    /*if (esp_http_client_get_transport_type(client) != HTTP_TRANSPORT_OVER_SSL) {
        ESP_LOGE(TAG, "Transport is not over HTTPS");
        return ESP_FAIL;
    }*/


make erase_flash flash

注意擦除