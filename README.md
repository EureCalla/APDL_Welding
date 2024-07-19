# APDL_Welding
### 程式碼核心介紹
🥑 此程式用於建立自動化機台焊接ANSYS模擬模型(包含長焊與點焊兩種工法)，並探討其焊接物料溫度、翹曲與應力等工況  
![image](https://github.com/EureCalla/APDL_Welding/blob/main/gif01.gif)
![image](https://github.com/EureCalla/APDL_Welding/blob/main/img02.png)
### 注意事項
1. 使用APDL語法撰寫並模型搭配使用ANSYS Workbench介面進行分析
2. 串接thermal-mechanical熱固耦合分析
   ![image](https://github.com/EureCalla/APDL_Welding/blob/main/step01.png)
4. 限制焊接路徑無法進行折返(若需折返請於模型中切成兩段)

### 程式碼介紹
thermal.txt ： 結構熱分析程式碼  
mechanical.txt ： 結構程式碼(input熱分析B.C.進行元素生死)

### Workbench中name_selection命名方式
![image](https://github.com/EureCalla/APDL_Welding/blob/main/step02.png)
1. 命名體積step1_%u%~10_%u%為點焊接工序順序
2. 命名節點s1_%u%~10_%u%為焊接起始點
3. 命名節點e1_%u%~10_%u%為焊接終點
4. _%u%代表點焊的同步項次
5. 命名體積zone1~10為外焊道
6. 命名節點start1~10為焊接起始點
7. %ARG1%代表焊接時溫度
8. %ARG2%代表點焊接速度
9. %ARG3%代表點銲接工序有幾個
10. %ARG4%代表最長點焊大約幾個點(抓取點數)
11. %ARG5%代表點焊總共求解切幾段
12. %ARG6%代表長焊接速度
13. %ARG7%代表長銲道總數目
14. %ARG8%代表長焊總共求解切幾段
