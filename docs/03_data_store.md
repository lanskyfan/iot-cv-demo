---
layout: post
title:  "数据存储于S3"
toc: true

---
通过IoT Core Rule Egine连接AWS Kinesis Firehose， 来将IoT设备生成的实时数据存储于S3中.

- 在进行此实验前，请先完成01_connected_publish中的全部内容。

## 1. 创建S3桶

- 此S3桶用于存储IoT设备生成的所有数据

- 进入S3控制台
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/1.png">
</a>

![Get started](./md_image/kinesis/1.png)

- 创建新的存储桶
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/2.png">
</a>

![Get started](./md_image/kinesis/2.png)

- 给存储桶命名，这里命名为iot-data
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/3.png">
</a>

![Get started](./md_image/kinesis/3.png)

- 之后按照默认设置创建存储桶
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/4.png">
</a>

![Get started](./md_image/kinesis/4.png)

<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/5.png">
</a>

![Get started](./md_image/kinesis/5.png)

## 2. 建立Kinesis Firehose

- 进入Kinesis服务
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/6.png">
</a>

![Get started](./md_image/kinesis/6.png)

- 点击入门
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/7.png">
</a>

![Get started](./md_image/kinesis/7.png)

- 选择使用Kinesis Firehose，创建传送流
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/8.png">
</a>

![Get started](./md_image/kinesis/8.png)

- 为新的传输流命名，这里命名为IoT-to-S3-Example
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/9.png">
</a>

![Get started](./md_image/kinesis/9.png)

- 禁用记录转换
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/10.png">
</a>

![Get started](./md_image/kinesis/10.png)

- 选择目标为S3
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/11.png">
</a>

![Get started](./md_image/kinesis/11.png)

- 选择刚刚创建的S3存储桶，并加上前缀iot-to-s3-example/，然后进行到下一步
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/12.png">
</a>

![Get started](./md_image/kinesis/12.png)

- 选择缓冲区大小为5MB，缓冲时间间隔为100秒， 并禁用S3压缩
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/13.png">
</a>

![Get started](./md_image/kinesis/13.png)

- 可选启用错误日志记录
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/14.png">
</a>

![Get started](./md_image/kinesis/14.png)

- 点击新建或选择IAM角色
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/15.png">
</a>

![Get started](./md_image/kinesis/15.png)

- 这时您将跳转至新的网页，按照默认的角色摘要直接创建
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/16.png">
</a>

![Get started](./md_image/kinesis/16.png)

- 返回刚才的网页，您将看到创建的IAM角色，点击进行下一步
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/17.png">
</a>

![Get started](./md_image/kinesis/17.png)

- 检查刚刚的配置后，创建传送流
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/18.png">
</a>

![Get started](./md_image/kinesis/18.png)

- 稍等片刻，您将看到您创建的传送流状态变为活跃
<a data-fancybox="gallery" href="https://iot-demo-resource.s3-ap-southeast-1.amazonaws.com/kinesis/19.png">
</a>

![Get started](./md_image/kinesis/19.png)