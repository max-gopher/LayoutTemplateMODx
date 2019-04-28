# LayoutTemplateMODx
Для работы с этим шаблоном должны быть установленны:

* [NodeJS](https://nodejs.org/en/) 
* [npm](https://www.npmjs.com/) - усанавливается вместе с NodeJS

Так же глобально должны быть установленны:

* [Gulp](https://gulpjs.com/): `npm i gulp -g` 
* [Bower](https://bower.io/): `mpn i bower -g`

Пример использования
--------------------

Клонируем репозиторий в `assets/layout`. Вытаскиваем все содержимое из папки LayoutTemplateMODx на уровень выше.
В командной строке переходим в `assets/layout` и выполняем `npm i`. После установки всех необходимых пакетов, пробуем собрать проект командой `gulp build`.

####Пример базовой tpl для Fenom:

``` html

<!doctype html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <base href="{'site_url' | config}">
    <title>{$_modx->resource.pagetitle ?: $_modx->resource.longtitle}</title>

    {block 'styles'}
        <link rel="stylesheet" href="{'assets_url' | config}layout/dist/css/main.min.css">
    {/block}
</head>
<body>

    <header class="header">
        <div class="header__block-info">
            <div class="container">
                <div class="header__logo">
                    <a href="{'site_url' | config}" class="header__logo-link">
                        <img src="{'assets_url' | config}images/logo.jpg" alt="{'site_name' | config}" class="header__logo-img">
                    </a>
                </div>
                <div class="header__callback">
                    <a href="javascript:;" class="header__callback-btn btn --callback">
                        <span class="header__callback-btn-stat"><i class="p-icon --callback"></i>Абхазия</span>
                        <span class="header__callback-btn-hov">Заказать звонок</span>
                    </a>
                </div>
                <div class="header__auth">
                    <a href="javascript:;" class="header__auth-link">
                        <span class="header__auth-link-icon p-icon --user"></span>Кабинет клиента</a>
                </div>
            </div>
        </div>
        <div class="header__block-nav">
            <nav class="container"></nav>
        </div>
    </header>



    {block 'template'}{/block}

    <footer class="footer">
        <div class="footer__social">
            <div class="container">
                <ul class="footer__social-list">
                    <li class="footer__social-item">
                        <a href="javascript:;" class="footer__social-link">
                            <span class="footer__social-link-icon p-icon --twit"></span>
                        </a>
                    </li>
                    <li class="footer__social-item">
                        <a href="javascript:;" class="footer__social-link">
                            <span class="footer__social-link-icon p-icon --fb"></span>
                        </a>
                    </li>
                    <li class="footer__social-item">
                        <a href="javascript:;" class="footer__social-link">
                            <span class="footer__social-link-icon p-icon --vk"></span>
                        </a>
                    </li>
                </ul>
            </div>
        </div>

        <div class="footer__nav">
            <div class="container">
                <div class="footer__nav-item">
                    <p class="footer__nav-item-title">Информация</p>
                    <ul class="footer__nav-item-list">
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">Юридическая</a>
                        </li>
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">о Доставке</a>
                        </li>
                    </ul>
                </div>
                <div class="footer__nav-item">
                    <p class="footer__nav-item-title">Мой аккаунт</p>
                    <ul class="footer__nav-item-list">
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">Личный кабинет</a>
                        </li>
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">Корзина</a>
                        </li>
                    </ul>
                </div>
                <div class="footer__nav-item">
                    <p class="footer__nav-item-title">Сервис</p>
                    <ul class="footer__nav-item-list">
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">Контакты</a>
                        </li>
                        <li class="footer__nav-item-list-item">
                            <a href="#" class="footer__nav-item-list-item-link">Site Map</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="footer__copyright">
            <div class="container">
                <p class="footer__copyright-text">© 2018-{'' | date : 'Y'}</p>
            </div>
        </div>
    </footer>

    {block 'scripts'}
        <script src="{'assets_url' | config}layout/dist/js/scripts.min.js"></script>
    {/block}
</body>
</html>

``` 
Приятного использования!

Благодарность
-------------

Не было бы этого шаблона без этих ребят: [optimizedhtml-start-template](https://github.com/agragregra/optimizedhtml-start-template)