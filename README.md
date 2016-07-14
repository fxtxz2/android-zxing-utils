[![bintray](https://api.bintray.com/packages/zyl/maven/android-zxing-utils/images/download.svg)](https://bintray.com/zyl/maven/android-zxing-utils/_latestVersion)
# android-zxing-utils
利用[ZXing](https://github.com/zxing/zxing)中的QRCodeWriter类获得BitMatrix来一个个检查颜色，重新获得构建一个像素矩阵获取一个全新的bitmap对象来表现二维码。参考[Android 生成带logo的二维码](http://www.jianshu.com/p/9a1387840cd6)

# 指南
## 生成二维码
```Java
QRbitmap = QRCodeUtils.getInstance().createQRCode(content, smallerDimension, 0xff000080, 0xffffffff);
```
content：二维码内容（如网址）  
smallerDimension:二维码尺寸  
0xff000080:二维码颜色块颜色值  
0xffffffff:二维码背景块颜色值
## 生成带logo的二维码
```Java
QRbitmap = QRCodeUtils.getInstance().createQRCodeWithLogo(content, smallerDimension, logoBitmap, 0xff000080, 0xffffffff);
```
content：二维码内容（如网址）  
smallerDimension:二维码尺寸  
logoBitmap:二维码中央logo图片bitmap  
0xff000080:二维码颜色块颜色值  
0xffffffff:二维码背景块颜色值
# Gradle
```Gradle
compile 'com.zyl.androidqrcode:android-zxing-utils:0.0.1'
```
