# 第2次作業題目-作業-HW2
>
>學號：113111117
><br />
>姓名：官益正
><br />
>作業撰寫時間：180 
><br />
>最後撰寫文件日期：2026/10/31 
>

1. 

a.![玩家按了W](image.png)
![玩家按了A](image-1.png)
![玩家按了S](image-2.png)
![玩家按了D](image-3.png)

Ans:
程式碼：

using UnityEngine;
using UnityEngine.InputSystem;

public class RabbitController : MonoBehaviour
{
    void Update()
    {
        // 取得目前電腦的鍵盤狀態
        Keyboard keyboard = Keyboard.current;

        // 判斷目前是否有連接或偵測到鍵盤
        // 如果 keyboard 為 null，代表目前沒有偵測到鍵盤
        if (keyboard == null)
        {
            // 結束這次 Update，不繼續執行下面的程式
            return;
        }

        // ==============================
        // 偵測 W 鍵
        // ==============================

        // wasPressedThisFrame 代表這一個影格剛好按下 W 鍵
        if (keyboard.wKey.wasPressedThisFrame)
        {
            // 在 Unity Console 顯示玩家按下 W 鍵
            Debug.Log("玩家按了 W 鍵！");
        }

        // ==============================
        // 偵測 A 鍵
        // ==============================

        // 判斷這一個影格是否剛按下 A 鍵
        if (keyboard.aKey.wasPressedThisFrame)
        {
            // 在 Unity Console 顯示玩家按下 A 鍵
            Debug.Log("玩家按了 A 鍵！");
        }

        // ==============================
        // 偵測 S 鍵
        // ==============================

        // 判斷這一個影格是否剛按下 S 鍵
        if (keyboard.sKey.wasPressedThisFrame)
        {
            // 在 Unity Console 顯示玩家按下 S 鍵
            Debug.Log("玩家按了 S 鍵！");
        }

        // ==============================
        // 偵測 D 鍵
        // ==============================

        // 判斷這一個影格是否剛按下 D 鍵
        if (keyboard.dKey.wasPressedThisFrame)
        {
            // 在 Unity Console 顯示玩家按下 D 鍵
            Debug.Log("玩家按了 D 鍵！");
        }
    }
}


   
   
 b. ![W+A](image-5.png)
 ![W+S](image-6.png)
 ![W+D](image-7.png)
 ![A+S](image-8.png)
 ![A+D](image-9.png)
 ![S+D](image-10.png)

Ans:
程式碼：

using UnityEngine;
using UnityEngine.InputSystem;

public class RabbitController : MonoBehaviour
{
    void Update()
    {
        // 取得目前電腦的鍵盤狀態
        Keyboard keyboard = Keyboard.current;

        // 檢查是否有偵測到鍵盤
        if (keyboard == null)
        {
            // 沒有鍵盤就結束這次 Update
            return;
        }

        // ==============================
        // W + A 複合鍵偵測
        // ==============================

        // isPressed 代表目前按鍵是否處於按住的狀態
        // && 代表兩個條件必須同時成立
        // 也就是 W 鍵和 A 鍵都必須按住
        if (keyboard.wKey.isPressed && keyboard.aKey.isPressed)
        {
            // 在 Unity Console 顯示 W + A
            Debug.Log("玩家按了 W + A 鍵！");
        }

        // ==============================
        // W + S 複合鍵偵測
        // ==============================

        // 同時檢查 W 鍵和 S 鍵是否都處於按住狀態
        if (keyboard.wKey.isPressed && keyboard.sKey.isPressed)
        {
            // 顯示 W + S 的偵測結果
            Debug.Log("玩家按了 W + S 鍵！");
        }

        // ==============================
        // W + D 複合鍵偵測
        // ==============================

        // 同時檢查 W 鍵和 D 鍵是否都處於按住狀態
        if (keyboard.wKey.isPressed && keyboard.dKey.isPressed)
        {
            // 顯示 W + D 的偵測結果
            Debug.Log("玩家按了 W + D 鍵！");
        }

        // ==============================
        // A + S 複合鍵偵測
        // ==============================

        // 同時檢查 A 鍵和 S 鍵是否都處於按住狀態
        if (keyboard.aKey.isPressed && keyboard.sKey.isPressed)
        {
            // 顯示 A + S 的偵測結果
            Debug.Log("玩家按了 A + S 鍵！");
        }

        // ==============================
        // A + D 複合鍵偵測
        // ==============================

        // 同時檢查 A 鍵和 D 鍵是否都處於按住狀態
        if (keyboard.aKey.isPressed && keyboard.dKey.isPressed)
        {
            // 顯示 A + D 的偵測結果
            Debug.Log("玩家按了 A + D 鍵！");
        }

        // ==============================
        // S + D 複合鍵偵測
        // ==============================

        // 同時檢查 S 鍵和 D 鍵是否都處於按住狀態
        if (keyboard.sKey.isPressed && keyboard.dKey.isPressed)
        {
            // 顯示 S + D 的偵測結果
            Debug.Log("玩家按了 S + D 鍵！");
        }
    }
}



## 其他