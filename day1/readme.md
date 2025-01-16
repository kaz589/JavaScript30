# **01 - JavaScript Drum Kit**
>首次上傳：2025/01/16   

![](https://github.com/kaz589/JavaScript30/blob/main/day1/background.jpg)

## **主題**
透過JS使鍵盤按下後播放出對應按鍵的聲音，並同時產生一個特效，  
在按下其他鍵後會關閉該特效並於新按鍵中啟用。  


## **步驟**
#### Step1. 新增keydown listener
利用`window.addEventListener('keydown', playSound);`來監聽鍵盤動作。  
#### Step2. 建立function`playSound`
1. 利用傳入的e.keyCode來取得對應的`audio`標籤及該按鍵的`div`標籤
2. 判斷傳入的e.keyCode是否有對應的`audio`標籤，若無則退出
3. 使對應的`div`加上`playing`樣式，產生對應的典及特效
4. 使對應的`audio`播放時間為0
5. 播放對應的音檔
#### Step3. 新增transitionend listener
1. 偵測所有包含`className='key'`的元件
2. 當該元件觸發特效並結束時(`transitionend`)，呼叫`removeTransition`
#### Step4.  建立function`removeTransition`
1. 判斷傳入的propretyName是否為transform，若否則退出
2. 若為transform，則移除`playing`樣式
## **筆記**

## **疑問**
1.長按
