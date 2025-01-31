# Восстановить на виртуальной машине отдельные директории и файлы

Вы можете восстановить из резервной копии отдельные файлы и директории на любую из ВМ, подключенных к {{ backup-name }}:

{% list tabs %}

- Консоль управления

  1. В [консоли управления]({{ link-console-main }}) выберите каталог, в котором находится резервная копия.
  1. Выберите сервис **{{ backup-name }}**.
  1. Перейдите на вкладку ![backups](../../../_assets/backup/backups.svg) **Резервные копии**.
  1. Выберите резервную копию, из которой вы хотите восстановить отдельные файлы или директории.
  1. В открывшемся файловом менеджере отметьте файлы и директории, которые вы хотите восстановить.
  1. На нижней панели нажмите кнопку ![file](../../../_assets/backup/file.svg) **Добавить к списку файлов для восстановления**.
  1. Последовательно добавьте в список **К восстановлению** все файлы и директории, которые вы хотите восстановить.
  1. Нажмите кнопку **Восстановить файлы**.
  1. В открывшемся окне:
      * Выберите ВМ, в которую вы хотите восстановить файлы и директории.

        {% note info %}

        ВМ, на которую будут восстановлены файлы и директории, должна быть [подключена](../../concepts/vm-connection.md) к {{ backup-name }}.

        {% endnote %}

      * (опционально) Укажите, нужно ли перезагрузить ВМ после восстановления.
      * Выберите один из типов расположения, в котором вы хотите восстановить файлы:
        * **Исходное** — файлы будут восстановлены в директориях, в которых находились изначально.
        * **Пользовательское** — файлы будут восстановлены в указанную директорию.

          Для пользовательского расположения в открывшемся файловом менеджере выберите директорию, в которую вы хотите восстановить файлы. 
          
          Чтобы создать новую директорию, нажмите кнопку ![new-folder](../../../_assets/backup/new-folder.svg) **Создать** и задайте ее имя.

          {% note info %}

          Имя директории не должно содержать символы: `\`, `/`, `:`, `*`, `?`, `"`, `'`, `<`, `>`, `|`.

          {% endnote %}

  1. Выберите действие, которое вы хотите сделать при совпадении имен файлов из резервной копии и файлов на ВМ:
      * **Перезаписать все файлы в директории**.
      * **Перезаписать только существующие файлы**.
      * **Не перезаписывать. Файлы, которых нет в исходной директории, также не будут записаны**.
  1. Нажмите кнопку **Восстановить**.

  Вы можете посмотреть прогресс восстановления файлов из резервной копии на вкладке ![operations](../../../_assets/backup/operations.svg) **Операции** в столбце **Статус**.

{% endlist %}