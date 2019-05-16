# Wiki

// setup phpstrom for bitrix
https://www.youtube.com/watch?v=tDf8CeLJwQw

// exclude file for phpstorm's indexing
*min.js;*.log;*.xml;*.txt;*.map.js;*min.css;*.cab;*.jar;*.rar;*.zip;*.eot;*.ttf;*.svg;*.woff;*.woff2;*.png;*.gif;*.jpg;

// add composer package 
    - https://symfony.com/doc/current/components/var_dumper.html
    - https://github.com/Seldaek/monolog (need?)


// show variable
if ($USER->IsAdmin()){ 	echo '<pre>' . print_r($arResult["PRICES"], true) . '</pre>'; }

// delete property FILE
CIBlockElement::SetPropertyValuesEx(
    $PRODUCT_ID,
    CATALOG_ID,
    ['PHOTO' => [ "VALUE" => ["del" => "Y"]  ]]
);

// Anonymous
CSaleUser::GetAnonymousUserID()

// Как сделать чтобы компонент на главной не виден, а на других был виден?
if ($APPLICATION->GetCurPage(false) === '/') {
  ...
}
  or
if ($curPage = $APPLICATION->GetCurPage()) {
   if (($curPage != "/index.php"))  {
            ....
        }
}


// login
<? require($_SERVER["DOCUMENT_ROOT"] . "/bitrix/header.php");
$USER->Authorize(1);
LocalRedirect("/bitrix/admin/");


// При написании в шаблонах компонентов форм, отправляющих данные методом POST, в качестве action необходимо указывать константу POST_FORM_ACTION_URI:
<form method="post" action="<?=POST_FORM_ACTION_URI?>">
    * * *
</form>

// run script
<?php
$_SERVER["DOCUMENT_ROOT"] = "/home/hosting/www";
$DOCUMENT_ROOT = $_SERVER["DOCUMENT_ROOT"];
define("NO_KEEP_STATISTIC", true);
define("NOT_CHECK_PERMISSIONS", true);
set_time_limit(0);
define("LANG", "ru");
require($_SERVER["DOCUMENT_ROOT"]."/bitrix/modules/main/include/prolog_before.php");

//ваш код...

require($_SERVER["DOCUMENT_ROOT"]."/bitrix/modules/main/include/epilog_after.php");
?>


//---------------------------
Конфигурация xdebug для linux (взята из этотй статьи: https://habrahabr.ru/post/250323/ по причинам, описанным в ней же):
zend_extension=xdebug.so
xdebug.remote_autostart=on
xdebug.remote_enable=on
xdebug.remote_port=9001
xdebug.idekey="PHPSTORM"

Конфигурация xdebug для Windows (эта система умрет):
zend_extension="%путь до php%/ext/php_xdebug_21?212???.dll
xdebug.remote_autostart=on
xdebug.remote_enable=on
xdebug.remote_port=9001
xdebug.idekey="PHPSTORM" 
