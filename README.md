Задание 1
Повторить демонстрацию лекции (развернуть vpc, 2 веб сервера, бастион сервер).

terraform init
<img width="762" height="350" alt="image" src="https://github.com/user-attachments/assets/1b73cea7-60d4-46f4-babc-1be90c414c3a" />

terraform plan 
<img width="1084" height="544" alt="image" src="https://github.com/user-attachments/assets/9409bcb4-8ccb-46c0-93f0-ba06a6542914" />

terraform apply

<img width="1722" height="380" alt="image" src="https://github.com/user-attachments/assets/75fd0622-709c-424e-a3dd-e9d66233aadf" />

<img width="891" height="333" alt="image" src="https://github.com/user-attachments/assets/e93e42c5-dc1b-4d05-ba24-b01ce0bbe14e" />



Задание 2

С помощью ansible подключиться к web-a и web-b , установить на них nginx.(написать нужный ansible playbook)
Провести тестирование и приложить скриншоты развернутых в облаке ВМ, успешно отработавшего ansible playbook.

ansible-playbook -i hosts.ini install_postgresql.yml

<img width="1091" height="475" alt="image" src="https://github.com/user-attachments/assets/135af64e-9b85-4345-9bbb-a44070d1b41e" />
nginx доступен <img width="852" height="181" alt="image" src="https://github.com/user-attachments/assets/eea3d6ad-dfa3-4580-baf2-59a18154c8eb" />


Дополнительные задания (со звёздочкой)*
Можете решить эти задания, если хотите глубже и/или шире разобраться в материале.

Задание 3*
Выполните действия, приложите скриншот скриптов, скриншот выполненного проекта.

Добавить еще одну виртуальную машину.
Установить на нее любую базу данных.
Выполнить проверку состояния запущенных служб через Ansible.

<img width="1107" height="481" alt="image" src="https://github.com/user-attachments/assets/0679288e-e58c-42df-9834-f503d21fd7a0" />


Задание 4*
Изучите инструкцию yandex для terraform. Добейтесь работы паплайна с безопасной передачей токена от облака в terraform через переменные окружения.

Для этого:

Настройте профиль для yc tools по инструкции.
Удалите из кода строчку “token = var.yandex_cloud_token”. Terraform будет считывать значение ENV переменной YC_TOKEN.
Выполните команду export YC_TOKEN=$(yc iam create-token) и в том же shell запустите terraform.
Для того чтобы вам не нужно было каждый раз выполнять export - добавьте данную команду в самый конец файла ~/.bashrc
