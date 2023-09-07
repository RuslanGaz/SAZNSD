# Получение сведений о системе

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1. Ноутбук Acer

2. Ubuntu 22.04 LTS

3. Интерпретатор командной оболочки 5.1.16(1)-release


## План

1. Выполнение команд

2. Анализ результатов

## Ход работы


1. Получим сведения о версии ядра:

```bash
root@ruslan-Virtual-Machine:/home/ruslan# uname -a
Linux ruslan-Virtual-Machine 5.15.0-27-generic #28-Ubuntu SMP Thu Apr 14 04:55:28 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux
```

Версия ядра - 5.15.0-27-generic, дата компиляции ядра - 14 апреля 2022 года.

2. Далее можно получить сведения о процессоре:

```bash
ruslan@LAPTOP-FLCQFHF2:~$ cat /proc/cpuinfo | grep "model name"
root@lime-Virtual-Machine:/home/ruslan# cat /proc/cpuinfo | grep "model name"
model name	: 11th Gen Intel(R) Core(TM) i5-124000 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i5-124000 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i5-124000 @ 2.00GHz
model name	: 11th Gen Intel(R) Core(TM) i5-124000 @ 2.00GHz
```

В системе используются четыре выделенных ядра

3. Далее получим последние 30 строк логов системы:

```bash
root@ruslan-Virtual-Machine:/home/ruslan# dmesg | tail -n 30
[    8.710072] vmwgfx 0000:00:0f.0: [drm] Available shader model: SM_5.
[    8.715234] fbcon: svgadrmfb (fb0) is primary device
[    8.716004] Console: switching to colour frame buffer device 100x37
[    8.725776] systemd[1]: Started Journal Service.
[    8.736471] [drm] Initialized vmwgfx 2.19.0 20210722 for 0000:00:0f.0 on minor 0
[    8.743267] systemd-journald[422]: Received client request to flush runtime journal.
[    9.873015] vmw_vmci 0000:00:07.7: Using capabilities 0x1c
[    9.888611] Guest personality initialized and is active
[    9.898685] VMCI host device registered (name=vmci, major=10, minor=123)
[    9.898693] Initialized host personality
[    9.926411] cryptd: max_cpu_qlen set to 1000
[    9.996057] AVX2 version of gcm_enc/dec engaged.
[    9.996996] AES CTR mode by8 optimization enabled
[   12.549793] audit: type=1400 audit(1694054836.336:2): apparmor="STATUS" operation="profile_load" profile="unconfined" name="lsb_release" pid=786 comm="apparmor_parser"
[   12.550931] audit: type=1400 audit(1694054836.336:3): apparmor="STATUS" operation="profile_load" profile="unconfined" name="ippusbxd" pid=784 comm="apparmor_parser"
[   12.551395] audit: type=1400 audit(1694054836.336:4): apparmor="STATUS" operation="profile_load" profile="unconfined" name="nvidia_modprobe" pid=791 comm="apparmor_parser"
[   12.551406] audit: type=1400 audit(1694054836.336:5): apparmor="STATUS" operation="profile_load" profile="unconfined" name="nvidia_modprobe//kmod" pid=791 comm="apparmor_parser"
[   12.553020] audit: type=1400 audit(1694054836.336:6): apparmor="STATUS" operation="profile_load" profile="unconfined" name="/usr/bin/man" pid=787 comm="apparmor_parser"
[   12.553033] audit: type=1400 audit(1694054836.336:7): apparmor="STATUS" operation="profile_load" profile="unconfined" name="man_filter" pid=787 comm="apparmor_parser"
[   12.553038] audit: type=1400 audit(1694054836.336:8): apparmor="STATUS" operation="profile_load" profile="unconfined" name="man_groff" pid=787 comm="apparmor_parser"
[   12.558536] audit: type=1400 audit(1694054836.344:9): apparmor="STATUS" operation="profile_load" profile="unconfined" name="/usr/lib/snapd/snap-confine" pid=793 comm="apparmor_parser"
[   12.558547] audit: type=1400 audit(1694054836.344:10): apparmor="STATUS" operation="profile_load" profile="unconfined" name="/usr/lib/snapd/snap-confine//mount-namespace-capture-helper" pid=793 comm="apparmor_parser"
[   12.561755] audit: type=1400 audit(1694054836.344:11): apparmor="STATUS" operation="profile_load" profile="unconfined" name="/usr/sbin/cups-browsed" pid=794 comm="apparmor_parser"
[   12.771000] NET: Registered PF_VSOCK protocol family
[   14.004479] e1000: ens33 NIC Link is Up 1000 Mbps Full Duplex, Flow Control: None
[   14.006541] IPv6: ADDRCONF(NETDEV_CHANGE): ens33: link becomes ready
[   17.020551] loop9: detected capacity change from 0 to 8
[   20.803828] rfkill: input handler disabled
[   40.305459] rfkill: input handler enabled
[   68.862158] rfkill: input handler disabled
```

## Оценка результата

В результате лабораторной работы была получена базовая информация об используемой системе.

## Вывод

Таким образом мы научились, используя команды оболочки bash, собирать и анализировать необходимую нам информацию о системе.
