# Steam

 онлайн-сервис цифрового распространения компьютерных игр и программ, разработанный и поддерживаемый компанией Valve. Steam выполняет роль средства технической защиты авторских прав, платформы для многопользовательских игр и потокового вещания, а также социальной сети для игроков. Программный клиент Steam также обеспечивает установку и регулярное обновление игр, облачные сохранения игр, текстовую и голосовую связь между игроками.

 ## Установка из репозитория
**Stream** можно установить любым привычным и удобным способом

**Установка через терминал**

::: code-group

```shell[apt-get]
su -
apt-get update
apt-get install steam
```
```shell[epm]
epm -i steam
```
:::

## Как поменять язык в Steam

Запустите клиент и найдите в верхней части приложения надпись Steam. При нажатии на нее откроется контекстное меню, выберите пункт Settings. В настройках перейдите в раздел Interface и кликните на English, чтобы открыть меню языков. В выпадающем списке выберите «Русский» и нажмите OK. После этого появится окно с информацией о том, что для применения изменений нужно перезапустить приложение. Нажмите Restart. Теперь Стим должен запуститься на русском языке.

![steam_1](/steam/steam_1.gif)

## Steam Play

Proton — инструмент, выпущенный Valve Software, который интегрирован со Steam Play, чтобы сделать игру в Windows-игры на Linux такой же простой, как нажатие кнопки "Играть" в Steam. Внутри Proton содержит другие популярные инструменты, такие как Wine и DXVK, которые игроку в противном случае пришлось бы устанавливать и поддерживать самостоятельно.

Запустите клиент и найдите в верхней части приложения надпись Steam. При нажатии на нее откроется контекстное меню, выберите пункт Настройки. В настройках перейдите в раздел Совсестимость и выберите:

* Включить Steam Play, для подержимаемых продуктов
* Включить Steam Play для других продуктов 
* Включить другие игры с помощью `Proton 8.x.x`

Включить поддержку Steam Play возможно и для конкретной игры. В разделе **БИБЛИОТЕКА** в перечне с играми выберите из списка игру, вызовите контекстное меню правой кликом мышки и выберите пункт свойства. В окне настроек в разделе **Совместимость**, активируйте опции **Принудительно использовать выбранный инструмент совместимости Steam Play** и выберите ветку **Proton**   

![steam_1](/steam/steam_2.gif)

## Проверить совместимость игр в Steam Play

[ProtonDB](https://www.protondb.com/) — база отчётов от игроков с пользовательскими оценками. Растущий выбор предложений позволяет настраивать игры, пока Proton продолжает улучшаться. В дополнении к этому, вы можете изучить каталог игр.

## Запуск клиента Steam для графических устройств от AMD

Для запуска клиента Steam требуется установить дополнительные пакеты:

::: code-group

```shell[apt-get]
su -
apt-get install vulkan-amdgpu xorg-drv-amdgpu i586-xorg-drv-amdgpu
```
```shell[epm]
epm -i vulkan-amdgpu xorg-drv-amdgpu i586-xorg-drv-amdgpu
```
:::

## Запуск клиента Steam для графических устройств от INTEL

Для запуска клиента Steam требуется установить дополнительные пакеты:

::: code-group

```shell[apt-get]
su -
apt-get install i586-libGL i586-libGLU i586-xorg-dri-intel
```
```shell[epm]
epm -i i586-libGL i586-libGLU i586-xorg-dri-intel
```
:::

## Не работают клавиши управления в игре при нативном запуске(без proton)

Проверьте что при запуске игры в вашей системе выбрана английская раскладка клавиатуры. Если это не так то, закройте игру, поменяйте раскладку на английскую и запустите игру заново.

Так-же можно добавить параметр запуска к игре, это должно решить проблему:
```shell
-input_button_code_is_scan_code
```

![Параметр запуска](./public/steam/steam_3.png)