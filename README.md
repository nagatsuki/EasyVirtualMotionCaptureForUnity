![icon](https://github.com/gpsnmeajp/EasyVirtualMotionCaptureForUnity/blob/README-image/ExternalReceiver.gif?raw=true)
# EasyVirtualMotionCaptureForUnity(ExternalReceiver)
VirtualMotionCaptureのUDP姿勢情報を受信してUnityシーンに反映します。

# 使い方動画
https://youtu.be/FhGqtzXEEQg

# 前提環境
sh_akiraさんのVirtualMotionCapture(v0.35～)が必要です。  
https://sh-akira.github.io/VirtualMotionCapture/  
  
**※旧バージョン(～v0.34)では使えません！！！！**  
先行リリース版はFanboxで提供されています。  
https://www.pixiv.net/fanbox/creator/10267568

動作確認済み環境
+ Windows 10
+ UniVRM-0.53.0_6b07
+ uOSC v0.0.2
+ Unity 2018.1.6f1

# お問合せ先
discordサーバー: https://discord.gg/QSrDhE8  
twitter: https://twitter.com/@seg_faul  

**注意！**  
**VMCとUnityで同じVRMを読み込むようにしてください！**  

# 使い方
## ExternalReceiverPackを使う場合(かんたん)
0. Unityを準備する
1. ExternalReceiverPackをダウンロードして新しい3Dプロジェクトに入れる  
https://github.com/gpsnmeajp/EasyVirtualMotionCaptureForUnity/releases/tag/v2.2  
2. 読み込みたいVRMファイル入れて、ExternalReceiverSceneを開いて配置する(あるいはExternalReceiverプレハブを配置する)
3. Scene ViewでExternalReceiverに、読み込んだVRMのGameObjectを「Model」に割り当てる
4. 再生して実行開始(VirtualMotionCaptureを起動してOSC送信開始状態にしてください)

以下を同梱しています。
+ [UniVRM-0.53.0_6b07(MIT Licence)](https://github.com/vrm-c/UniVRM/blob/master/LICENSE.txt)
+ [uOSC v0.0.2(MIT Licence)](https://github.com/hecomi/uOSC/blob/master/README.md)

![配置例](https://github.com/gpsnmeajp/VMC_ExternalReceiver/blob/README-image/img3.png?raw=true)

## 一から準備する場合
0. Unityを準備する
1. ExternalReceiver.csをダウンロードして、動かしたいプロジェクトに入れる
2. UniVRMをダウンロードして、動かしたいプロジェクトに入れる  
https://github.com/vrm-c/UniVRM/releases
3. uOSCをダウンロードして、動かしたいプロジェクトに入れる  
https://github.com/hecomi/uOSC/releases
4. 読み込みたいVRMファイル入れて、Sceneに配置する
5. Scene ViewでCreate Empty
6. Inspectorで、ExternalReceiver.csと、uOSC Serverを割り当てる
7. ExternalReceiverに、読み込んだVRMのGameObjectを「Model」に割り当てる
8. uOSC ServerのPortをVirtualMotionCaptureに合わせる(デフォルト: 39539)
9. 再生して実行開始(VirtualMotionCaptureを起動して送信開始状態にしてください)

# How to use
## ExternalReceiverPack (Easy)
0. Open Unity project.
1. Download ExternalReceiverPack and install.
https://sabowl.sakura.ne.jp/gpsnmeajp/vmc/ExternalReceiverPack_v2_1.unitypackage
2. Drag&Drop your VRM file, and Open "ExternalReceiverScene", Place VRM Model.  
 (or put "ExternalReceiver" prefab on your scene)
3. put VRM Model game object on ExternalReceiver's "Model" in Scene View.
4. Let's Play. (And turn on VirtualMotionCaputres OSC Function)

## Manualy Setup
0. Open Unity project.
1. Download "ExternalReceiver.cs" and put in.
2. Download "UniVRM" and put in.
https://github.com/vrm-c/UniVRM/releases
3. Download "uOSC" and put in.
https://github.com/hecomi/uOSC/releases
4. Drag&Drop your VRM file, and Place VRM Model.  
5. "Create Empty" in Scene View.
6. Attach "ExternalReceiver.cs" and "uOSC Server"
7. put VRM Model game object on ExternalReceiver's "Model" in Scene View.
8. Set uOSC Server's "Port" to VirtualMotionCapture's Port. (Default: 39539)
9. Let's Play. (And turn on VirtualMotionCaputres OSC Function)

# Protocol
https://github.com/gpsnmeajp/EasyVirtualMotionCaptureForUnity/wiki/Protocol-V2

# 送信側の例
https://github.com/gpsnmeajp/VirtualMotionCapture/blob/v0.22basefix/Assets/ExternalSender/ExternalSender.cs

# Licence
CC0  
http://creativecommons.org/publicdomain/zero/1.0/deed.ja  

# 作者
gpsnmeajp  
https://sabowl.sakura.ne.jp/gpsnmeajp/  
