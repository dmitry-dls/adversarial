# adversarial
## Описание

```
adversarial.ipynb - ноутбук с проектом
adv_images.zip - результаты атаки в архиве
```

Остальные файлы: y_target_cuda.pt - форвард  для target_images, adv_stats.csv - значения переменных, лоссов и ссим с индексами из pairs_list.csv, adv_imgs/ - атакованные изображения, изображения вносимых изменений и градиенты.

Исходные данные:
resnet18.py, resnet18_scale_fold0_best.pth.tar, resnet50.py, best_model_chkpt-resnet50.t7, imgs.zip, pairs_list.csv.

[Ссылка на папку](https://drive.google.com/open?id=1kFAfbwnc0i5UKQQ5QeaU_LM6DnkH83if)

## Контакты

Ид профиля в канвасе: `24795191`

Имя: `dmitryg`

[Ссылка на папку](https://drive.google.com/open?id=1kFAfbwnc0i5UKQQ5QeaU_LM6DnkH83if) на гугл-диске со всеми файлами. 

## Как сделать чтобы всё заработало

Скопировать все данные из папки по ссылке на гугл-диск, 
смонтировать его в ноутбуке, и в переменной `drive_path` заменить путь на свой.

Сохранить ноутбук и запустить всё.

```
%%bash
echo "Copying data and model"
drive_path="/content/drive/My Drive/MFTI/Final/Adversarial_Attacks"  <-- ЗДЕСЬ
for file in $(ls "$drive_path"); do
    if [ ! -e $file ]; then
    cp --verbose "$drive_path/$file" .
    fi
done
```

