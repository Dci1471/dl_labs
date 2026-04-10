# Лабораторная работа №3
## Сегментация
[веса лучшей модели](https://drive.google.com/file/d/1jAzj6UHcvJx8QLNuxunZwGdCUJTH2OTC/view?usp=sharing)
## Описание

- Архитектура модели efficientnet-b2  + UnetPlusPlus
- LR 3e-4, img_sz 512, extract_edges
- Аугментации HorizontalFlip, VerticalFlip, RandomRotate90, RandomBrightnessContrast, CoarseDropout
- Loss функция: (DiceLoss + BCEWithLogitsLoss + FocalLoss) + edge_weights * BCEWithLogitsLoss
- планировщик: CosineAnnealingWarmRestarts
- сегментации маски и обнаружения граней

Результат 91.1% Public Score
