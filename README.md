# 問卷送出後呼叫多個 Webhook

## **不會程式沒關係！SurveyCake 手把手教學，讓你三分鐘就上手**

讓你的問卷表單沒有極限！

問卷送出後，除了呼叫單一 Webhook，有時因為需要串接多個系統，例如將問卷填達送到 POS 機與 CRM 系統，必須呼叫多支 API，進行更多深入的運用。

這篇文章將會介紹如何在問卷送出後呼叫複數個 Webhook API：

問卷送出後呼叫複數個 Webhook API

1. 建立一份 SurveyCake 問卷
2. 建立 Google App Script
3. 設定問卷 Webhook Url
4. 測試填答問卷

## 1. 建立一份 SurveyCake 問卷

### **1–1. [登入後台](http://bit.ly/2VUOcE8) > [建立問卷](https://blog.surveycake.com/%E5%A6%82%E4%BD%95%E5%A5%97%E7%94%A8-surveycake-%E5%95%8F%E5%8D%B7%E7%AF%84%E6%9C%AC-%E4%B8%80%E9%8D%B5%E5%BB%BA%E7%AB%8B%E5%AE%8C%E6%95%B4%E5%95%8F%E5%8D%B7%E8%A1%A8%E5%96%AE-e97a2ab90adf) > 儲存**

首先，在進行串接之前你必須先建立一份 SurveyCake 問卷。

## 2. 建立 Google App Script

### 2-1 點擊 [此處](https://raw.githubusercontent.com/orientalist/surveycakeHookSwitcher/main/index.js) ****後會跳出一程式碼頁面，全選複製所有程式碼****

![螢幕擷取畫面_20230204_080921.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/%25E8%259E%25A2%25E5%25B9%2595%25E6%2593%25B7%25E5%258F%2596%25E7%2595%25AB%25E9%259D%25A2_20230204_080921.png)

### ****2-2 前往 [Google App Script](https://script.google.com/home) 建立一個新專案**

![Group 1.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/Group_1.png)

### 2-3 將**`程式碼.gs`**預設文字清空後，**貼上**剛剛全選複製的程式碼（3–1）

![螢幕擷取畫面_20230204_081155.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/%25E8%259E%25A2%25E5%25B9%2595%25E6%2593%25B7%25E5%258F%2596%25E7%2595%25AB%25E9%259D%25A2_20230204_081155.png)

```
* 小提醒：
點擊指令碼編輯器時，「程式碼.gs」裡會出現以下程式碼：
function myFunction() {
}
請記得先把上述程式碼刪除清空，再貼上剛剛於 3-1 處所全選複製的程式碼哦！
```

### 2-4 將您欲呼叫的多個 Webhook 網址加入**`程式碼.gs` 中的 `hooks` 內**

![Group 2.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/Group_2.png)

### 2-5 加入網址後按下****「 儲存 」、「執行」按鈕****

![Group 4.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/Group_4.png)

![Group 3.png](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/Group_3.png)

過程中可能需要您授權 google 帳號

![1_vxq8x-LNrY9lUBOgY1j-dQ.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_vxq8x-LNrY9lUBOgY1j-dQ.webp)

### 2-6 ****選擇上方工具列「 部署 > 網路應用程式 」****

![1_xjz1eGyWlwZg75851fm4Tg.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_xjz1eGyWlwZg75851fm4Tg.webp)

![1_7xFunStw4XBgzUHHQcUMLQ.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_7xFunStw4XBgzUHHQcUMLQ.webp)

- 將「執行身份」選擇為： **`請選擇你自己的 Google 帳號`**
- 「誰可以存取」請選擇：**`所有人。`**
- 點擊右下方按鈕 **`部署`**
- 完成授權後即可取得網址，請「**複製」**該網址

![1_6_JDDJ_kEX56DEcHC2kPtw.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_6_JDDJ_kEX56DEcHC2kPtw.webp)

![1_ERnpS2ux23o6zyWilax06g.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_ERnpS2ux23o6zyWilax06g.webp)

## 3 設定問卷 Webhook Url

### 3-1 ****貼上「Webhook Url」後按下「儲存」****

回到問卷後台的 Webhook 頁面，於「 Webhook URL 」中貼上剛剛複製的網址（2-6）。

![1_MOZrgj0sfBrRS_HsmQ8C_A.webp](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_MOZrgj0sfBrRS_HsmQ8C_A.webp)

![別忘了點選右上角的儲存按鈕，webhook 網址才會被儲存起來哦！](%E5%95%8F%E5%8D%B7%E9%80%81%E5%87%BA%E5%BE%8C%E5%91%BC%E5%8F%AB%E5%A4%9A%E5%80%8B%20Webhook%208b130db62f46428487224d4ec601b233/1_TuobMxtAiiLqj2ekdiFLRw.webp)

別忘了點選右上角的儲存按鈕，webhook 網址才會被儲存起來哦！

## 4 測試填答問卷

### 4****–1 打開問卷網址進行填答並送出，您即可以檢查期望被呼叫的系統是否有被正確觸發!****