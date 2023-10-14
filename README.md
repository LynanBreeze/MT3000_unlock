# MT3000_unlock

Thanks to **iBelieve**'s script, this is a shortcut for applying his script to unlock MT3000's hidden features.
Original Resource In Here: [[经验分享] 【2023.8.2】官方UI辅助脚本: 快速登录LuCI、美化、快捷按钮](https://forum.gl-inet.cn/forum.php?mod=viewthread&tid=3129)

## Firstly, connect your MT3000 via SSH

```
ssh root@192.168.8.1
```

## Then, run this script on below
```
cd /www && TARGET_FILE="gl_home.html" && cp $TARGET_FILE "${TARGET_FILE}.back" && sed -i '/\<\/html\>/d' $TARGET_FILE && SCRIPT_URL="https://raw.githubusercontent.com/LynanBreeze/MT3000_unlock/main/script.txt" && curl -s "$SCRIPT_URL" >> "$TARGET_FILE" && echo "</html>" >> "$TARGET_FILE"
```

## If you have network problem with `raw.githubusercontent.com`, try this instead:

```
cd ~ && cd /www && TARGET_FILE="gl_home.html" && cp $TARGET_FILE "${TARGET_FILE}.back" && sed -i '/\<\/html\>/d' $TARGET_FILE && SCRIPT_URL="https://raw.githubusercontent.com/LynanBreeze/MT3000_unlock/main/script.txt" && curl -s "$SCRIPT_URL" >> "$TARGET_FILE" && echo "</html>" >> "$TARGET_FILE"
```

## All set! Refresh your router admin page in your browser, you should see the changes has been made.
