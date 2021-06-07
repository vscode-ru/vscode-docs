<p align="center">
  <img alt="vscode logo" src="images/logo-stable.png" width="100px" />
  <h1 align="center">Документация Visual Studio Code</h1>
</p>

Вы нашли репозиторий GitHub документации Visual Studio Code, который содержит контент для [документации Visual Studio Code](https://code.visualstudio.com/docs).

Отправленные здесь темы будут опубликованы на портале [Visual Studio Code](https://code.visualstudio.com).

Если вы ищете репозиторий GitHub продукта VS Code, вы можете найти его [здесь](https://github.com/microsoft/vscode).

## Указатель

- [Указатель](#указатель)
- [Visual Studio Code](#visual-studio-code)
- [Обратная связь](#обратная-связь)
- [Проблемы с документацией](#проблемы-с-документацией)
- [Содействие](#содействие)
  - [Рабочий процесс](#рабочий-процесс)
  - [Клонирование](#клонирование)
    - [Клонирование без двоичных файлов](#клонирование-без-двоичных-файлов)
- [Публикация](#публикация)

## Visual Studio Code

[VS Code](https://code.visualstudio.com/) - это легкий редактор исходного кода и мощная среда разработки для создания и отладки современных веб-приложений, мобильных и облачных приложений. Это бесплатно и доступно на вашей любимой платформе - Linux, macOS и Windows.

Если вы попали сюда в поисках другой информации о VS Code, перейдите на [наш веб-сайт](https://code.visualstudio.com) для получения дополнительной информации.

## Обратная связь

Если вы хотите оставить отзыв о документации, используйте элемент управления обратной связью, расположенный в нижней части каждой страницы документации.

## Проблемы с документацией

Чтобы сообщить об ошибках в документации, создайте [новую проблему GitHub](https://github.com/microsoft/vscode-docs/issues). Пожалуйста, сначала проверьте, существует ли проблема.

Если вы считаете, что проблема связана с самим продуктом VS Code, укажите проблемы в репозитории продукта VS Code [здесь](https://github.com/microsoft/vscode/issues).

## Содействие

Чтобы добавить новые темы/информацию или внести изменения в существующую документацию, прочтите [Правила участия](./CONTRIBUTING.md#contributing).

### Рабочий процесс

Два предлагаемых рабочих процесса:

- Для небольших изменений используйте кнопку «Изменить» на каждой странице, чтобы отредактировать файл Markdown прямо на GitHub.
- Если вы планируете внести значительные изменения или предварительно просмотреть файлы Markdown в VS Code, [клонируйте](#cloning) репозиторий и [редактируйте и просматривайте](https://code.visualstudio.com/docs/languages/markdown) файлы прямо в VS Code.

![Кнопка предварительного просмотра Markdown](images/MDPreviewButton.png)

### Клонирование

1. Установите [Git LFS](https://git-lfs.github.com/).
2. Запустите `git lfs install`, чтобы настроить глобальные хуки git. Вам нужно запустить это только один раз для каждой машины.
3. `git clone git@github.com:Microsoft/vscode-docs.git`.
4. Теперь вы можете использовать двоичные файлы `git add` и зафиксировать их. Они будут отслеживаться в LFS.

#### Клонирование без двоичных файлов

Возможно, вы захотите клонировать репозиторий без изображений размером 1,6 ГБ. Вот шаги:

1. Установите [Git LFS](https://git-lfs.github.com/).
2. Запустите `git lfs install`, чтобы настроить глобальные хуки git. Вам нужно запустить это только один раз для каждой машины.
3. Клонируйте репо без двоичных файлов.
    - macOS / Linux: `GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:Microsoft/vscode-docs.git`.
    - Windows: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone git@github.com:Microsoft/vscode-docs.git`.
4. Теперь вы можете выборочно проверять некоторые двоичные файлы для работы. Например:
    - `git lfs pull -I "docs/nodejs"` для загрузки изображений только в `docs/nodejs`
    - `git lfs pull -I "release-notes/images/1_4*/*"` для загрузки изображений только в `release-notes/images/1_4*`
    - `git lfs pull -I "docs,api"` для загрузки всех изображений в `docs` и `api`
    - `git lfs pull -I <PATTERN>`, если `<PATTERN>` является допустимым [шаблон включения и исключения Git LFS](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-fetch.1.ronn#include-and-exclude).

Историю этого репозитория до внедрения LFS можно найти по адресу [microsoft/vscode-docs-archive](https://github.com/microsoft/vscode-docs-archive).

## Публикация

Инструкции по публикации изменений документации можно найти [здесь](https://github.com/microsoft/vscode-website#publishing-a-documentation-change) в (приватном) репозитории веб-сайта VS Code.
