# 非Esim手机使用 Hotlink eSIM 相关研究

## 前言

因为长期换sim卡导致丢失过几次后，这次也是下定决心研究一下esim。因为还是不想换手机（绝对不是因为穷），所以基于作者**Unicorn369** 所贡献的**HookEuicc**我展开尝试并且成功获取到esim代码（非二维码）

## 原理

1. 准备环境
安装Hotlink APP，并且完成登录，且可以找到切换esim的选项。
需要注意的是余额需要＞RM 5 以支付转换费用。
确保设备已经获得 Root 权限。
在 LSPosed 环境。
安装 HookEuicc 模块。
2. 实操过程
在LSPosed中勾选Hotlink，且选中原作者所示的必要支持部分，源自原作者项目的提示如下：
> [!NOTE]
> 需勾选 `com.android.se` 并重启手机 (或执行 `su -c killall com.android.se`)

在我在使用时 HookEuicc显示不在工作，但是实测可以。
打开Hotlink App 进行转换 这时已经没有不符合转换要求的提示了 
完成KYC 完成后Hotlink 显示失败 但是粘贴板复制了ESim的相关信息了（有提示），而后我黏贴到写入卡的位置就可以正常激活了
## 总结
理论上和实践上都是完全ok的 非常感谢作者**Unicorn369** 开发 因为我看确实是很少人使用Hotlink去转ESim 所以我个人也没有看见例如 Giffgaff那样比较便捷的平台，不过大概率是因为KYC的缘故吧 
综上 流程完成 总体来说还是特别顺利的 再次感谢作者**Unicorn369**以及所贡献的**HookEuicc**
