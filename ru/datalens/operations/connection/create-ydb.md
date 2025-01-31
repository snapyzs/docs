# Создание подключения к {{ ydb-name }}

{% note info %}


Для создания подключения вам потребуется [сервисный аккаунт](../../../iam/concepts/users/service-accounts.md) с [ролью](../../../iam/operations/sa/assign-role-for-sa.md) **ydb.viewer** (или **viewer**).


Для написания подзапросов в датасетах и запросов в QL-чартах используйте [синтаксис YQL](https://ydb.tech/ru/docs/yql/reference/syntax/).

{% endnote %}

Чтобы создать подключение к {{ ydb-name }}:


{% include [datalens-workbooks-collections-note](../../../_includes/datalens/operations/datalens-workbooks-collections-note.md) %}



1. Перейдите на [страницу подключений]({{ link-datalens-main }}/connections).


1. Нажмите кнопку **Создать подключение**.

1. Выберите подключение **{{ ydb-short-name }}**.

1. Укажите параметры подключения:

   
   * **Облако и каталог**. Выберите каталог, в котором будет находиться ваш сервисный аккаунт.
   * **Сервисный аккаунт**. Выберите существующий сервисный аккаунт или создайте новый.
   * **База данных**. Выберите подключаемую базу данных или создайте новую.


   {% note warning %}

   В именах столбцов базы данных {{ ydb-short-name }} не допускается использование заглавных букв.

   {% endnote %}
   
   * **Время жизни кеша в секундах**. Укажите время жизни кеша или оставьте значение по умолчанию. Рекомендованное значение — 300 секунд (5 минут).
   * **Уровень доступа SQL запросов**. Позволяет использовать произвольный SQL-запрос для [формирования датасета](../../concepts/dataset/settings.md#sql-request-in-datatset).

1. Нажмите кнопку **Создать подключение**.
1. Укажите название подключения и нажмите кнопку **Создать**.

{% include [datalens-check-host](../../../_includes/datalens/operations/datalens-check-host.md) %}
