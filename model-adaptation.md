Ссылка на найденную сеть для сегментации изображений в высоком качестве: [HF](https://huggingface.co/lkeab/hq-sam), [github](https://github.com/syscv/sam-hq), [spaces](https://huggingface.co/spaces/sam-hq-team/sam-hq
)

Ссылка на репозиторий для доменной адаптации: [github](https://github.com/thuml/Transfer-Learning-Library)

![Алгоритм сегмантации](images/image1.png)

Рис 1. Алгоритм сегмантации изображения

## Используем метод Domain Adversarial Neural Network (DANN) для адаптации модели для сегментации изображений
### Инструкция (для linux)
1. Создать виртуальное окружение
```
python -m venv venv
```
2. Активировать виртуальное окружение 
```
source venv/bin/activate
```
3. Скопировать репозиторий
```
git clone https://github.com/thuml/Transfer-Learning-Library
```
4. Перейти в директорию Transfer-Learning-Library
```
cd Transfer-Learning-Library
```
5. Запустить setup.py
```
python setup.py install
```
6. Установить необходимые зависимости
```
pip install -r requirements.txt
```
7. Запустить адаптацию
```
CUDA_VISIBLE_DEVICES=0 python dann.py "путь к данным" -d "имя датасета" -s "исходный домен" -t "целевой домен" -a "архитектура модели" --epochs "количество эпох" --log "путь для логов"
```
