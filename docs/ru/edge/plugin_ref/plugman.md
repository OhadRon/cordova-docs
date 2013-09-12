---

license: Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

           http://www.apache.org/licenses/LICENSE-2.0
    
         Unless required by applicable law or agreed to in writing,
         software distributed under the License is distributed on an
         "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
         KIND, either express or implied.  See the License for the
         specific language governing permissions and limitations
    

   under the License.
---

# Использование Plugman для управления расширениями

Начиная с версии 3.0 Cordova реализует все API устройства как плагины и оставляет их не подключенными по умолчанию. Также поддерживается два различных способа добавления и удаления плагинов. Во-первых, с помощью `cordova CLI` через интерфейс командной строки. Во-вторых, с помощью интерфейса командной строки нижнего уровня [plugman][1]. Это руководство основано на втором подходе, который может быть полезен для разработчиков, желающих обновить свою версию Cordova, но которые еще не применяли Cordova CLI на практике.

 [1]: https://github.com/apache/cordova-plugman/

Для дополнительной информации о plugman смотрите [файл README в репозитории][2].

 [2]: https://github.com/apache/cordova-plugman/blob/master/README.md

## Основные команды

Чтобы установить plugman, вам потребуется установить [node.js][3] на свою машину:

 [3]: http://nodejs.org/

    npm install -g plugman
    

Вот синтаксис добавления плагина вне зависимости от выбранной платформы:

    plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin <name|url|path> [--plugins_dir <directory>] [--www <directory>] [--variable <name>=<value> [--variable <name>=<value> ...]]
    

Для удаления плагина:

    plugman --uninstall --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin <id> [--www <directory>] [--plugins_dir <directory>]
    

## Установка модулей ядра

Приведенные ниже примеры показывают, как добавлять плагины по мере необходимости, так чтобы любой Cordova API, который вы используете в вашем проекте, по-прежнему продолжил работать после обновления до версии 3.0. Для каждой команды, необходимо выбрать целевую платформы, и ссылаться на каталог проекта платформы.

*   cordova-plugin-battery-status plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-battery-status.git

*   cordova-plugin-camera plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-camera.git

*   cordova-plugin-console plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-console.git

*   cordova-plugin-contacts plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-contacts.git

*   cordova-plugin-device plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device.git

*   cordova-plugin-device-motion (accelerometer) plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device-motion.git

*   cordova-plugin-device-orientation (compass) plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-device-orientation.git

*   cordova-plugin-dialogs plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-dialogs.git

*   cordova-plugin-file plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-file.git

*   cordova-plugin-file-transfer plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-file-transfer.git

*   cordova-plugin-geolocation plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-geolocation.git

*   cordova-plugin-globalization plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-globalization.git

*   cordova-plugin-inappbrowser plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git

*   cordova-plugin-media plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-media.git

*   cordova-plugin-media-capture plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-media-capture.git

*   cordova-plugin-network-information plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-network-information.git

*   cordova-plugin-splashscreen plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-splashscreen.git

*   cordova-plugin-vibration plugman --platform <ios|android|blackberry10|wp7|wp8> --project <directory> --plugin https://git-wip-us.apache.org/repos/asf/cordova-plugin-vibration.git