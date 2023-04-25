# fedora_install
cheat sheet

gnome的系统代理还是很好用的

安装google 专门支持中文程序员的字体和配置字体的

```bash
sudo dnf install google-noto-cjk-fonts gnome-tweaks
```

然后 字体统一使用`Noto Sans Mono CJK SC`，`SC` 代表着简体中文


改键位用
kmonad

test.kbd
```
(defcfg
  input  (device-file "/dev/input/by-id/usb-1fc9_Gaming_Keyboard-if01-event-kbd")
  output (uinput-sink "My KMonad output")
  fallthrough false
  allow-cmd false
)

(defsrc
  esc  f1   f2   f3   f4   f5   f6   f7   f8   f9   f10  f11  f12        ssrq slck pause
  grv  1    2    3    4    5    6    7    8    9    0    -    =    bspc  ins  home pgup  nlck kp/  kp*  kp-
  tab  q    w    e    r    t    y    u    i    o    p    [    ]    \     del  end  pgdn  kp7  kp8  kp9  kp+
  caps a    s    d    f    g    h    j    k    l    ;    '    ret                        kp4  kp5  kp6
  lsft z    x    c    v    b    n    m    ,    .    /    rsft                 up         kp1  kp2  kp3  kprt
  lctl lmet lalt           spc            ralt rmet cmp  rctl            left down rght  kp0  kp.
)

(deflayer test
  caps  f1   f2   f3   f4   f5   f6   f7   f8   f9   f10  f11  f12        ssrq slck pause
  grv  1    2    3    4    5    6    7    8    9    0    -    =    bspc  ins  home pgup  nlck kp/  kp*  kp-
  tab  q    w    e    r    t    y    u    i    o    p    [    ]    \     del  end  pgdn  kp7  kp8  kp9  kp+
  esc a    s    d    f    g    h    j    k    l    ;    '    ret                        kp4  kp5  kp6
  lsft z    x    c    v    b    n    m    ,    .    /    rsft                 up         kp1  kp2  kp3  kprt
  lalt lmet lctl           spc            rctl rmet cmp  ralt            left down rght  kp0  kp.
)
```
```
[Unit]
Description=kmonad keyboard config

[Service]
Restart=always
RestartSec=3
ExecStart=/bin/bash -c "sleep 0.5 && /usr/local/bin/kmonad /etc/kmonad/config.kbd"
Nice=-20

[Install]
WantedBy=default.target
```


flatpak obsidian



https://extensions.gnome.org/extension/615/appindicator-support/   tray icon

