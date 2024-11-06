# CameraXFragment

![icon](https://user-images.githubusercontent.com/15169396/147327054-5065aafc-5bb3-4477-8877-21b39212f4a9.png)


使用CameraX 简单的封装了拍照，录制视频的CameraXFragment,可以实现类似微信录像拍照效果，点击拍照 长按录像



## 依赖
   First，   
   
       repositories {
        google()
        mavenCentral() // 添加mavenCentral 依赖，Google 已经停止Jcenter
       }

   Second，   
   
       implementation "io.github.anylifezlb:CameraXFragment:2.x.latest" //请根据version log 升级
       
       
       
## 使用说明

        val cameraConfig=CameraConfig.Builder()
            .flashMode(CameraConfig.FLASH_MODE_OFF) //默认是关闭的
            .mediaMode(CameraConfig.MEDIA_MODE_ALL) //视频拍照都可以
            .cacheMediasDir(cacheMediasDir) //还没有适配存储分区，2022会的
            .build()

        cameraXFragment = CameraXFragment.newInstance(cameraConfig)

        supportFragmentManager.beginTransaction()
            .replace(R.id.fragment_container, cameraXFragment).commit()


### 更多说明请下载体验Demo
![image](https://user-images.githubusercontent.com/15169396/142362234-4300c052-cee6-4a1d-b835-baab7ae9e9b6.png)

