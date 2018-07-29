# Kaggle-Rental-Listing-Inquiries
Xgboost

## 1 任务说明：
    Rental Listing Inquiries 数据集是 Kaggle 平台上的一个分类竞赛任务。
    需要根据公寓的特征来预测其受欢迎程度（用户感兴趣程度分为高、中、低三类）。
    其中房屋的特征 x 共有 14 维，响应值 y 为用户对该公寓的感兴趣程度。
    评价标准为 logloss。
    
    数据链接：https://www.kaggle.com/c/two-sigma-connect-rental-listing-inquiries
    
## 2 数据说明：
    为减轻对特征工程的入手难度，以及统一标准，数据使用特征工程编码后的数据：
    RentListingInquries_FE_train.csv，或稀疏编码的形式：RentListingInquries_FE_train.bin 
    xgboost 既可以单独调用，也可以在sklearn 框架下调用。
    若采用 xgboost 单独调用使用方式，建议读取稀疏格式文件。
    
    关于特征工程的过程，可参看文件：FE_RentListingInqueries.ipynb
    
## 3 特征字段说明：
    bathrooms: 浴室的数量
    bedrooms: 卧室的数量
    building_id：
    created：发布时间
    description：一些描述
    display_address：展出地址
    features: 公寓的一些特征
    latitude：纬度
    listing_id
    longitude：经度
    manager_id：管理ID
    photos: 租房图片集
    price: 美元
    street_address：街道地址
    interest_level: 目标变量，受欢迎程度. 有三个类: ‘high’, ‘medium’, ‘low’
