# CameraXFragment


<img src="https://github.com/PangHaHa12138/CameraXFragment/blob/main/app/src/main/ic_launcher-playstore.png" width="300px">


使用CameraX 简单的封装了拍照，录制视频的CameraXFragment,可以实现类似微信录像拍照效果，点击拍照 长按录像


### 截图

<img src="https://github.com/PangHaHa12138/CameraXFragment/blob/main/screenshot/Screenshot_2024-11-06-13-44-43-586_com.zenglb.cameraxfragment.jpg" width="400px">

       
## 使用说明

        val cameraConfig=CameraConfig.Builder()
            .flashMode(CameraConfig.FLASH_MODE_OFF) //默认是关闭的
            .mediaMode(CameraConfig.MEDIA_MODE_ALL) //视频拍照都可以
            .cacheMediasDir(cacheMediasDir) //还没有适配存储分区，2022会的
            .build()

        cameraXFragment = CameraXFragment.newInstance(cameraConfig)

        supportFragmentManager.beginTransaction()
            .replace(R.id.fragment_container, cameraXFragment).commit()





