# SRv6 深度學習：實驗檔案

實驗有六個 XRd vRouter 節點（PE1、P2、P3、P4、P5、PE6）和兩台 Alpine Linux 主機（CE-A、CE-B）。
路由器執行 IOS XR 26.2.2。實驗使用 CML 2.10.0 或 2.10.1。

## 檔案

- `srv6-lab-v3.yaml`：拓撲檔。這是 CML 原生格式的實驗檔，請在 CML 用 Import Lab 匯入。它列出節點、連線，以及每個節點的啟動設定。路由器使用節點定義 `xrd-vr-e1000` 與映像定義 `xrd-vr-e1000-26-2-2`，這是 CML 裡的自訂映像檔。請先建立它，或把檔案中的名稱改成你自己的名稱。每台路由器使用 2 vCPU 與 7168 MiB。
- `configs/<node>.cfg`：實驗結束時每台路由器的 running configuration。這是第 19 集之後的狀態。PE1 的 Gi0/0/0/4 是不受信任的邊界埠，套用 ACL SRV6-BOUNDARY-IN。在這個狀態下，PE1 上的 VPWS 是中斷的。
- `CE-addressing.md`：兩台 CE 主機的介面位址（英文）。

## 開始之前

- 這些檔案沒有真正的密碼。實驗檔中，使用者 cisco 的密碼是 CHANGE-ME。`.cfg` 檔已移除密碼行。請設定你自己的密碼。
- 動態 SID 的值在重新啟動後會改變。請從 SID 表讀取，不要從影片抄寫。
- 節點 stop 再 start 後，XR 設定會保留。wipe 會讓節點回到實驗檔中的啟動設定。

## 授權

Copyright 2026 Quintus Zhu。採用 CC BY-NC-ND 4.0：https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh-hant
第三方文件與商標屬於各自的所有者。
