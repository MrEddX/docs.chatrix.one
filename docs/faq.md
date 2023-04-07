# Често Задавани Въпроси

<figure markdown>
  ![Често задавани въпроси](resources/img/faq.jpeg){ width="800" }
  <figcaption>Често задавани въпроси при използване на <b>Chatrix.One</b></figcaption>
</figure>

При наличие на технически проблеми, както и при нужда от помощ във връзка с използването на **Chatrix.One**, можете да изпратите запитване под формата на имейл или **XMPP** съобщение до администратор. Моля, преди това да проверите дали вече не е отговорено на Вашия въпрос в редовете по-долу. Благодаря!

!!! info "Информация"

    За работа с търсачката :fontawesome-solid-magnifying-glass: можете да използвате следните бързи клавиши:

    * ++slash++ ++f++ ++s++ - активират режим търсене
    * <kbd>↓</kbd> <kbd>↑</kbd> - следващ, предишен резултат
    * ++enter++ - избор на резултат
    * ++esc++ - деактивира режим търсене

## Какво представлява услугата?

**Chatrix.One** е сървър предлагащ комуникация, базирана на **XMPP** протокол. Можете да изпращате съобщения, емотикони, снимки, гласови и видео съобщения, местоположение и файлове. На разположение са още гласова и видео връзка.

* * *

## Какво представлява **XMPP**?

!!! info "Информация"

    **XMPP** - **Ex**tensible **M**essaging and **P**resence **P**rotocol

Най-лесният начин да обясня принципа и предимствата на **XMPP**, е да го сравня с електронната поща. Ако искате да си създадете Ваш собствен имейл адрес, достатъчно е да изберете доставчик (сървър) и да регистрирате профил (акаунт). Например в *abv.bg*, *gmail.com*, *mail.bg* или друг. Името на избрания от Вас профил заедно с адреса на доставчика, свързани посредством символа :fontawesome-solid-at:, образуват Вашия имейл адрес. Например *pesho@dostavchik.com*. От този момент вече можете да обменяте имейли с потребители регистрирани на различни сървъри без проблем. Потребител на *abv.bg*, може да напише имейл до потребител на *gmail.com* или който и да било друг доставчик. Това е възможно, тъй като доставчиците обменят съобщения помежду си, без потребителят да е ангажиран по някакъв начин с това. Предимствата са очевидни. Потребителите могат свободно да избират своя доставчик и все пак всеки може да общува с всеки. За изпращането на съобщения не се изисква нищо друго освен профил за електронна поща, при който и да е доставчик, и адрес на получателя. На подобен принцип работи и **XMPP**. Избирате сървър и получавате свобода да комуникирате с потребители от други сървъри. Освен, че можете да създавате няколко профила при един доставчик, е възможно да създавате и множество профили при различни доставчици. Дали има смисъл от това е друг въпрос. Възможно е **XMPP** услугата да бъде ограничена само в рамките на вътрешната мрежа на дадена организация. Директен достъп през Интернет до такъв сървър не е възможен. Комуникацията се извършва само сред служителите и то ако са свързани към вътрешната мрежа, директно или чрез [**VPN**](https://en.wikipedia.org/wiki/Virtual_private_network).

На графиката по-долу е представен принципът на на работа на **XMPP** комуникацията.

```mermaid

flowchart RL
    subgraph <b>ИНТЕРНЕТ</b>
        subgraph Потребители на <b>Chatrix.One</b>
        CHATRIX[(<b>XMPP</b> Сървър <br><br> <b>chatrix.one</b>)]
        a((Потребител A)) <-.-> |5222| CHATRIX
        b((Потребител B)) <-.-> |5222| CHATRIX
        c((Потребител C)) <-.-> |5222| CHATRIX
        end

        subgraph Потребители на <b>abc.tld</b>
        ABC[(<b>XMPP</b> Сървър <br>fa:fa-server<br> <b>abc.tld</b>)]
        d((Потребител D)) <-..-> |port<br>5222| ABC
        e((Потребител E)) <-..-> |5222| ABC
        f((Потребител F)) <-..-> |5222| ABC
        end

        CHATRIX <====> |5269| ABC

        subgraph Потребители с повече от един профил
        g((Потребител G)) <-..-> |5222| CHATRIX & ABC
        h((Потребител H)) <-..-> |5222| CHATRIX & ABC
        end
    end

    subgraph <b>ВЪТРЕШНА МРЕЖA</b>
    LOCAL[(<b>XMPP</b> Сървър <br><br> <b>local.net</b>)]
    i((Потребител I)) <-.-> |5222| LOCAL
    j((Потребител J)) <-.-> |5222| LOCAL
    k((Потребител K)) <-.-> |5222| LOCAL
    l((Потребител L)) <-.-> |5222| LOCAL
    m((Потребител M)) <-.-> |5222| LOCAL
    end

```

!!! quote ""

    **Фиг.1** Модел на **XMPP** комуникация.

    - Комуникацията в локална мрежа е изолирана от сървърите с публичен достъп в Интернет пространството;<br>
    - Комуникацията клиент-сървър (**c2s**) се осъществява на порт 5222;<br>
    - Комуникацията сървър-сървър (**s2s**) се осъществява на порт 5269;<br>
    - Абонатите могат да притежават повече от един профил, както при един, така и при няколко **XMPP** доставчика.

Списък с безплатни **XMPP** сървъри, можете да намерите на страниците на [**XMPP Compliance Tester**](https://compliance.conversations.im/) и [**Jabber.at**](https://list.jabber.at/). Повече информация за **XMPP** протокола можете да прочетете и в [**Wikipedia**](https://bg.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol).

* * *

## От колко време съществува XMPP?

Протоколът се заражда през 1998г., но реално като платформа започва да функционира през 1999г. Хронологията е достъпна на официалната страница на [**XMPP**](https://xmpp.org/about/history/).

* * *

## Кой използва **XMPP**?

Протоколът се появява на бял свят още през далечната 1999г. За четвърт век история може спокойно да се каже, че е издържал теста на времето. Днес **XMPP** се използва от голям брой корпорации, което е породено от неговата стабилност и надеждност.
По-известни организациите използващи ежедневно **XMPP** са:

| Организация                   | Активни потребители дневно | Съобщения в секунда | Съобщения дневно  |
|:-----------------------------:|:--------------------------:|:-------------------:|:-----------------:|
| :fontawesome-brands-google: Google | ~ 2 000 000 000       |  -                  | -                 |
| :fontawesome-brands-apple: Apple   | ~ 500 000 000         |  -                  | -                 |
| :fontawesome-brands-whatsapp: WhatsApp | ~ 2 000 000 000   |  -                  | ~ 100 000 000 000 |
| Nintendo                      | ~ 34 000 000               |  ~ 600              | ~ 2 000 000 000   |
| League Of Legends             | ~ 27 000 000               |  ~ 11 000           | -                 |
| FORTNITE                      | ~ 300 000 000              |  ~ 400 000          | -                 |
| ZOOM                          | ~ 200 000 000              |  -                  | -                 |
| :fontawesome-brands-github: GitHub | -                     |  -                  | -                 |
| :fontawesome-brands-facebook: Facebook | -                 |  -                  | -                 |
| GMX                           | -                          |  -                  | -                 |
| Orange                        | -                          |  -                  | -                 |

За повече детайли вижте страницата на [**RST Software**](https://www.rst.software/blog/22-companies-using-xmpp-and-ejabberd-to-build-instant-messaging-services).

* * *

## Какво представлява **OMEMO**?

**OMEMO** представлява метод за двойно криптиране на комуникацията от край до край. Ключовете за криптиране автоматично се генерират за всяко едно съобщение, което прави комуникацията още по-сигурна. Иначе казано, дори да бъде компрометирано едно съобщение, останалата комуникация остава незасегната. Допълнителна информация за метода можете да намерите в [**Wikipedia**](https://en.wikipedia.org/wiki/OMEMO) и на интернет страницата на **Conversations** в раздела [**OMEMO**](https://conversations.im/omemo/).

* * *

## Как мога да регистрирам профил?

Пълна информация относно регистрирането на профил в **Chatrix.One** е налична в раздела [Регистрация](https://docs.chatrix.one/account/registration/).

* * *

## Има ли публикуван шаблон на имейл за регистрация?

Шаблон на примерен имейл за регистрация е наличен в раздела [Регистрация](https://docs.chatrix.one/account/registration/#_3).

* * *

## Има ли публикуван шаблон на **XMPP** съобщение за регистрация?

Шаблон на примерно **XMPP** съобщение за регистрация е налично в раздела [Регистрация](https://docs.chatrix.one/account/registration/#_3).

* * *

## Кой клиент препоръчвате?

Използвам **Gajim** под **Windows** и **Linux**. За **Android** използвам **Conversations** - платена версия. И двата клиента са със 100% **OMEMO** съвместимост и са с отворен код. За **iOS** не мога да дам мнение, тъй като никога не съм разполагал с устройство работещо под тази операционна система.

* * *

## Защо да избирам платена версия, след като има безплатна?

Аз лично, съм избрал платената версия на **Conversations**, защото по този начин подпомагам разработчика на приложението [**Daniel Gultsch**](https://gultsch.de/), който допринесе изключително много за развитието на **XMPP** през последните години. Също негова е заслугата за внедряването на **OMEMO**, като стандарт в **XMPP** комуникацията. В крайна сметка изборът е изцяло Ваш.

* * *

## От къде мога да сваля клиент за моята операционна система?

Подробна информация, относно наличните клиенти за работа с **Chatrix.One** в зависимост от операционната система която използвате, можете да намерите в раздел [Клиенти](https://docs.chatrix.one/clients/). За Ваше удобство връзките за сваляне са публикувани и в редовете по-долу.

=== ":fontawesome-brands-windows: Windows"

    | Клиент   |Безплатен           |  Отворен код       | Линк                                        |
    |:---------|:------------------:|:------------------:|:-------------------------------------------:|
    |**Gajim** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**Gajim.org**](https://gajim.org/download) |

=== ":fontawesome-brands-linux: Linux"

    | Клиент   | Безплатен          |  Отворен код       | Линк                                         |
    |:---------|:------------------:|:------------------:|:--------------------------------------------:|
    |**Gajim** | :fontawesome-solid-check: |  :fontawesome-solid-check: | [**Gajim.org**](https://gajim.org/download) |
    |**Dino**  | :fontawesome-solid-check: |  :fontawesome-solid-check: | [**Dino.im**](https://dino.im/#download)    |

=== ":fontawesome-brands-apple: macOS"

    | Клиент   | Безплатен          |  Отворен код       | Линк                                                                     |
    |:---------|:------------------:|:------------------:|-------------------------------------------------------------------------:|
    |**Gajim** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**Gajim.org**](https://dev.gajim.org/gajim/gajim/-/wikis/help/Gajim-on-macOS) |
    |**Beagle IM** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**Mac App Store**](https://apps.apple.com/us/app/beagleim-by-tigase-inc/id1445349494) |

=== ":fontawesome-brands-google-play: Android"

    | Клиент           | Безплатен          |  Отворен код       | Линк                                                                |
    |:-----------------|:------------------:|:------------------:|:-------------------------------------------------------------------:|
    |**Conversations** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**F-droid**](https://f-droid.org/packages/eu.siacs.conversations/) |
    |**Conversations** | **7.79лв**         | :fontawesome-solid-check: | [**Google Play**](https://play.google.com/store/apps/details?id=eu.siacs.conversations) |

=== ":fontawesome-brands-apple: iOS"

    | Клиент   | Безплатен          |  Отворен код       | Линк                                                                       |
    |:---------|:------------------:|:------------------:|:--------------------------------------------------------------------------:|
    |**Monal** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**App Store**](https://apps.apple.com/us/app/monal-xmpp-chat/id317711500) |

=== ":fontawesome-brands-firefox: Web"

    | Клиент         | Безплатен          |  Отворен код       | Линк                                                         |
    |:---------------|:------------------:|:------------------:|:------------------------------------------------------------:|
    |**Converse.js** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**Conversejs.org**](https://conversejs.org/fullscreen.html) |

=== ":fontawesome-solid-terminal: CLI"

    | Клиент       | Безплатен          |  Отворен код       | Линк                                                |
    |:-------------|:------------------:|:------------------:|:---------------------------------------------------:|
    |**Profanity** | :fontawesome-solid-check: | :fontawesome-solid-check: | [**Profanity-IM**](https://profanity-im.github.io/) |

* * *

## Мога ли да имам няколко профила, регистрирани на различни сървъри?

Можете да имате колкото профила пожелаете, както на един, така и на на различни сървъри. Възможно е дори да ги управлявате от едно и също устройство. Единствено ще трябва да се впишете с всеки отделен профил поотделно в настройките на софтуера, който използвате.

* * *

## Кои клиенти поддържат **OMEMO**?

Клиенти със 100% OMEMO съвместимост:

- **Conversations**;
- **Converse.js**;
- **Dino**;
- **Gajim**;
- **Monal**;
- **Chat Secure**;
- **Profanity**.

Изброените по-горе са тествани с изключение на **Monal** и **Chat Secure**. Подробен списък с клиенти и тяхната съвместимост е наличен на сайта [**Are We OMEMO Yet?**](https://omemo.top/).

* * *

## Как мога да разбера дали използвам **OMEMO**?

Ако съобщенията  в **Conversations** са придружени с индикатор *"чекнат щит"* :material-shield-check: това е сигурен знак, че използвате **OMEMO**. В **Gajim** проверете за наличието на зелено оцветен символ *"щит"* :material-shield: до датата и часа на съобщенията. Той ще бъде изцяло оцветен, когато сте се доверили на устройството. В случай, че не сте добавили устройството към списъка с доверени устройства, символът "щит" ще бъде наполовина оцветен в зелено. За всички останалите приложения ситуацията е аналогична.

!!! warning "Внимание"

    В случай, че съобщенията не са криптирани в **Conversations** ще бъдат изписани на червен фон. В **Gajim** ще виждате отключен катинар с оранжев символ `!` върху него. Намира се отдясно на лентата в която пишете.

* * *

## Мога ли да използвам друг метод на криптиране?

Можете да използвате и **OpenPGP**, но Ви препоръчвам преди това да се запознаете с възможните проблеми със сигурността на този метод. За повече информация вижте страницата на модула - [**XEP-0027: Current Jabber OpenPGP Usage**](https://xmpp.org/extensions/xep-0027.html) и по-точно частта [**Security Considerations**](https://xmpp.org/extensions/xep-0027.html#security).

* * *

## Мога ли да използвам **OTR** криптиране?

Поддръжката на **OTR** методът на криптиране е преустановена, поради неговата уязвимост към атаки от типа [**Man-In-The-Middle**](https://en.wikipedia.org/wiki/Man-in-the-middle_attack). За повече информация вижте страницата на модула - [**XEP-0364: Current Off-the-Record Messaging Usage**](https://xmpp.org/extensions/xep-0364.html) и по-точно частта [**Security Considerations**](https://xmpp.org/extensions/xep-0364.html#security).

* * *

## Криптирана ли е гласовата комуникация?

В случай, че сте активирали метод на криптиране (**OMEMO** или **OpenPGP**) аудио комуникацията също ще бъде криптирана. В приложението **Conversations** това ще бъде отбелязано със зелено оцветен символ *"чекнат щит"* :material-shield-check: в горния ляв ъгъл на екрана.

* * *

## Криптирана ли е видео комуникацията?

В случай, че сте активирали метод на криптиране (**OMEMO** или **OpenPGP**) видео комуникацията също ще бъде криптирана. В приложението **Conversations** това ще бъде отбелязано със зелено оцветен символ *"чекнат щит"* :material-shield-check: в горния ляв ъгъл на екрана.

* * *

## Как да възстановя забравена парола?

Ако не Ви познавам лично, ще се наложи да си я спомните. В противен случай, регистрирайте нов профил. Паролата е единственият начин да удостоверите, че точно Вие сте собственикът на профила.

!!! tip "Съвет"

     Следващият път използвайте софтуер за управление на пароли (**Password Manager**). Бих препоръчал [**Bitwarden**](https://bitwarden.com/).

* * *

## Как да променя паролата?

Проверете в секцията за настройки на профил в приложението което използвате. Например:

- **Gajim**

`Avatar Picture` → `General` → `Login` → `Change Password`

- **Conversations**

`Основен екран` → `Меню с трите точки` → `Управление на акаунти` → `Избираме акаунт` → `Трите точки` → `Смяна на парола`

За останалите клиенти процедурата е аналогична.

* * *

## Поддържа ли се двуфакторно удостоверяване?

Метод за удостоверяване от типа [**Second Factor Authentication**](https://en.wikipedia.org/wiki/Multi-factor_authentication), познат още като **Multi Factor Authentication** (**2FA**, **MFA**), към момента не е интегриран в **XMPP** услугата предлагана от **Chatrix.One**. Удостоверяването става само с потребителско име и парола. Именно поради тази причина Ви съветвам да проявите разум в избора на парола. Съвети относно избора на парола, ще намерите в раздел [Регистрация](https://docs.chatrix.one/account/registration/).

* * *

## Мога ли да изтрия профил?

Да. Стъпките са подобни на тези при смяната на парола. В секцията за настройка на акаунт имате опция за изтриването му. За мобилни приложения докоснете и задръжте върху самия профил. Ще видите опция изтриване.

* * *

## Има ли някакви правила, които трябва да спазвам?

Разбира се. Правила има и те са задължителни за всички. Моля, да се запознаете с тях в раздела [Правила](https://docs.chatrix.one/terms/).

* * *

## Длъжен ли съм да пища само на кирилица?

Можете да пишете на какъвто език пожелаете, стига да спазвате [правилата](https://docs.chatrix.one/terms/) за ползване на услугата.

* * *

## На колко устройства мога да използвам услугата?

На практика нямате ограничения. Само имайте предвид, че добавянето на всяко ново устройство води до отпадане на доверието във вашите кореспонденти. Иначе казано, ще трябва да Ви се доверят отново, било то чрез "сляпо доверяване" или чрез сканиране на [**QR**](https://bg.wikipedia.org/wiki/QR_код) код от екрана на някое от вашите активни устройства.

* * *

## Какво означава "Сляпо доверяване" или "**Blind Trust**"?

Накратко, това е начин да се доверите на устройство притежавано от човека с когото комуникирате, без да сте 100% сигурни, че от отсрещната страна действително стои той. Най-сигурният начин за извършване на доверяване е, като сканирате **QR** кода от екрана на устройство, собственост на Вашия кореспондент. Достатъчно е да сканирате само едно от  устройствата. Ще забележете, че колкото повече устройства притежавате, толкова по-сложен става **QR** кодът. Това е така, защото в него се съдържат идентификаторите на всички устройства от Вашия профил. Подробна информация можете да намерите в публикацията [**Blind Trust Before Verification**](https://gultsch.de/trust.html)на на **Daniel Gultsch**.

* * *

## Ще знам ли дали отсреща са получили съобщението?

Да, ако потребителят е сред доверените Ви контакти. Под съобщението ще се появи символ :material-check:.

* * *

## Ще мога ли да коригирам грешно изпратени съобщения?

Да, ще можете да поправяте последното изпратено съобщение, като това ще бъде отразено с появата на символ :material-pencil: до датата и часа на съответното съобщение.

* * *

## Ще виждам ли дали от отсрещната страна ми пишат в момента?

Да. Ще виждате съобщение от типа *"Pesho is typing..."* или *"Пешо пише в момента..."*. Съответно има и съобщение, ако бъде преустановено писането.

* * *

## Мога ли да блокирам известяването за това дали пиша или не?

Да. Вижте в настройките на приложението, раздел **Privacy**.

* * *

## Ще знаят ли останалите дали съм на линия?

Да. Проверете дали сте разрешили тази опция. Обикновено това става от настройките на Вашето приложението, раздел **Privacy**.

* * *

## Ако кача грешен файл или картинка мога ли да ги изтрия?

Можете, но само от Вашето устройство. От сървъра и устройствата на други потребители това е невъзможно.

* * *

## Мога ли да създавам стаи?

Да. Можете да създавате стаи и да каните приятели в общ чат.

* * *

## Мога ли да създавам споделена група от типа **Shared Rooster Group**?

Не, но ако се свържете с мен мога да създам такава. По този начин няма да има нужда да каните всички членове по отделно. Групата ще бъде видима веднага в приложението на всички включени в нея. За връзка най-добре изпратете **XMPP** съобщение до администратор.

* * *

## Защо не получавам известия (нотификации) на мобилното устройство?

=== ":fontawesome-brands-android: Android"

    Вероятно използвате телефон без **Google Play Services** или **Google Cloud Messaging**.

    !!! success "Решение"

        Настройте приложението да работи в преден план.

=== ":fontawesome-brands-apple: iOS"

    - Вероятно използвате приложението **ChatSecure** и не сте разрешили опцията "**Push**" в настройките.

    !!! success "Решение"

        Проверете настройките на приложението. Също така, вижте и настройките на операционната система, по-точно частта касаеща статус на известяванията във фонов режим. Ако все още няма резултат пробвайте приложението **Monal**.

    - Батерията е изтощена или сте активирали режим за пестене на батерията.

    !!! success "Решение"

        Заредете батерията и изключете режима за пестене на батерията.

* * *

## Защо получавам съобщение за грешка при опит за регистрация?

Към момента регистрирането на профил, чрез формата за регистрация или през приложенията е забранено! Повече информация може да намерите в статията за [Регистрация](https://docs.chatrix.one/account/registration/#_2).

* * *

## Защо получавам съобщение за невалиден **SSL/TLS** сертификат?

Вероятно използвате устройство с остаряла операционна система (**Android** 6 или 7). Можете ръчно да приемете сертификата.

!!! warning "Внимание"

    Преди да приемете ръчно сертификат, **задължително** обърнете внимание и се уверете, че е регистриран за следните домейни: `chatrix.one`, `conference.chatrix.one`, `pubsub.chatrix.one`, `proxy.chatrix.one` и `upload.chatrix.one`. В противен случай може да станете жертва на така наречената хакерска атака от типа [**Man-In-The-Middle**](https://en.wikipedia.org/wiki/Man-in-the-middle_attack).

* * *

## Защо не мога да провеждам аудио и видео комуникация с **Gadjim**?

Вероятно използвате **Windows** като операционна система. Към момента **Gajim** поддържа аудио и видео комуникация само под **Linux**.

* * *

## Как да изключа архивирането на съобщенията?

Ако не желаете съобщенията да се съхраняват за определения период, имате възможност да изключите архивирането.

- **Conversations**

`Управление на акаунти` → `Избирате акаунт` → `Трите точки` → `Опции за архивиране` → `Никога`

- **Gajim**

`Avatar Picture` → `Privacy` → `Keep Chat History` → `Until Gajim is Closed`

За останалите клиенти процедурата е аналогична.

* * *

## Какви данни съхранявате на сървъра?

Подробна информация ще намерите в статията за [Поверителност](https://docs.chatrix.one/privacy/#_4).

* * *

## Какви данни се пренасят за осъществяване на **Push Notifications**?

Подробно описание може да прочетете на **Github** страницата на приложението [**Conversations**](https://github.com/iNPUTmice/p2/blob/master/README.md#conversations-push-proxy).

* * *

## Криптирани ли са снимките които качвам?

Да, но само и единствено, ако сте активирали криптиране от край до край, например **OMEMO**.

* * *

## Как би изглеждала снимка, която се съхранява на сървъра в криптиран вид?

Ако бъде свалена от сървъра и се направи опит да бъде разгледана на компютър или друго устройство, ще видите само и единствено чисто черен екран.

* * *

## След като имате достъп до сървъра, можете ли да декриптирате съобщенията и файлове на потребителите?

За декриптиране на комуникацията и файловете, съхранявани на сървъра, не е достатъчен само администраторски достъп. Нужни са още и ключовете с които е извършено криптирането, а те се се съхраняват на устройствата на потребителите. Следователно, не съм в състояние да осъществя достъп до комуникацията в четим вид.

!!! info "Информация"

    Едно от нещата към които се отнасям изключително отговорно е личната комуникация да остане наистина лична. За повече информация вижте раздела [Поверителност](https://docs.chatrix.one/privacy/).

* * *

## Ще бъде ли достъпна услугата след "**X**" години?

Понастоящем не се предвижда тази услуга да бъде закрита. Докато не изпадна във финансови затруднения или се появят други сериозни причини, ще предлагам **XMPP** услугата. Прекратяването, разбира се, ще бъде обявено своевременно.

!!! info "Информация"

    Ако желаете да подсигурите дългосрочното функциониране на **Chatrix.One**, можете да участвате във финансирането. При нужда от повече информация моля, свържете се с администратор.

* * *

## Какви разходи поражда такъв вид услуга?

- Закупуване на домейн, както и ежегодна такса;
- Ежемесечен наем за сървър - облачен или физически;
- Разходи за Интернет - генериран трафик;
- Разходи за електричество;
- Втори сървър - за съхраняване на резервни копия на критичната информация;
- Хардуер;
- Лично време.

* * *

## Защо въобще предлагате такава услуга?

Защото имам желание, възможност и време, но преди всичко това ми доставя огромно удоволствие.

* * *

## Защо е безплатна услугата?

Защото към момента мога да си го позволя.

* * *

## Колко е сигурна услугата?

Настоящите стандарти на **XMPP** позволяват много сигурен обмен на съобщения - просто трябва да ги използвате! Постоянно използвам най-новите методи за криптиране на сървъра и блокирам установяването на връзка по несигурни канали. Във връзка с намаляване полето за изява от страна на хакери съм забранил **SSH** достъпа, както и уеб базираната администрация на сървъра. Защитната стена ([**Firewall**](https://bg.wikipedia.org/wiki/Защитна_стена)) е настроена по-възможно най-ограничаващ начин. Комуникацията е подсигурена чрез **TLS** сертификат от [**ZeroSSL**](https://zerossl.com/) и [**Let's Encrypt**](https://letsencrypt.org/). Обмяната на ключове е посредством [**Diffie-Hellman**](https://bg.wikipedia.org/wiki/Дифи-Хелман).

* * *

## Колко е стабилна услугата?

Наблюденията ми върху **XMPP** базирана услуга от 2018г. до днес показват, че услугата е изключително стабилна. Към момента системата разполага с достатъчно [**RAM**](https://bg.wikipedia.org/wiki/Памет_с_произволен_достъп) памет, така че може да поеме няколко хиляди активни потребители по едно и също време.

* * *

## В крак ли сте с последните новости в областта на **XMPP**?

Веднага щом това стане технически възможно и разумно, на този сървър ще бъдат внедрени нови разширения на **XMPP** и най-добри практики. За мен е важна пълната съвместимост с водещия проект **Conversations**, който несъмнено помогна на **XMPP** да достигне нов блясък през последните години. Резултатът от теста на **Chatrix.One** можете да видите в онлайн [доклада за съответствие с **XMPP**](https://compliance.conversations.im/server/chatrix.one/)).

* * *

## Каква база данни използвате?

Използвам [**PostgreSQL**](https://www.postgresql.org/).

* * *

## В четим вид ли се съхраняват паролите?

Не. Паролите са криптирани посредством [**SCRAM-SHA1**](https://wiki.xmpp.org/web/SASL_Authentication_and_SCRAM#SCRAM-SHA-1(-PLUS)) механизъм.

* * *

## Защо се казва **Chatrix.One**?

Защото е преди всичко **Chat**. Първоначалният замисъл беше да се използва само сред роднини **R**elatives, хостваше се на **I**ntel NUC  и е базирана на **X**MPP. Окончанието  **One** - защото е единственият метод за такъв тип комуникация, от който се нуждая към момента. И не на последно място, защото домейнът беше свободен.

```mermaid
flowchart BT
    A[<b>Chat</b>] ---> |Chat| R(<b>Chatrix.One</b>)
    B[<b>R</b>elatives] ---> |r| R
    C[<b>I</b>ntel NUC] ---> |i| R
    D[<b>X</b>MPP] ---> |x| R
    E[<b>One</b>] ---> |One| R
```

* * *

## Колко хора се занимават с администрацията?

Към момента съм единствен човек, което си има предимства и недостатъци.

!!! warning "Внимание!"

    Основен недостатък: [**Bus Factor**](https://bg.wikipedia.org/wiki/Bus_factor) = 1

* * *

## Колко ток харчи?

С цел минимална консумация на електричество, използвам процесор базиран на **ARM** архитектура. При 100% натоварване на всичките четири ядра, консумацията достига 10.4W. През по-голямата част от времето сървърът е натоварен под 10%.

* * *

## Защо **Ejabberd**, а не **Prosody**?

Има много причини за решението ми да избера **Ejabberd**. Повечето от тях се основават на недостатъците, които намирам в **Prosody**, а те вероятно няма да бъдат отстранени скоро:

- **Prosody** изразходва повече системна памет. Положението се подобри малко с `mod_external_upload` и новите версии на кода за свързване с **PostgreSQL**, но все още има какво да се желае;
- **Prosody** използва само едно ядро на процесора;
- Не може да бъде надграждан в клъстър;
- В бъдеще, ако има нужда не бих могъл да предоставя услуга от типа **High Availability**;
- Понякога не е в крак с новите **XMPP** стандарти, изисквани от приложението **Conversations** за **Android**;
- За гласова и видео връзка изисква инсталиране на допълнителен [**STUN**](https://en.wikipedia.org/wiki/STUN)/[**TURN**](https://en.wikipedia.org/wiki/Traversal_Using_Relays_around_NAT) сървър.

**Ejabberd** има някои предимства пред **Prosody**:

- Разработчиците имат дългогодишен опит с **XMPP** - **Ejabberd** е много зряла платформа;
- Езикът [**Erlang**](https://bg.wikipedia.org/wiki/Erlang), на който е написан **Ejabberd**, е създаден точно за този вид приложения и е известен с високата си производителност;
- **Ejabberd** използва всички налични ядра на процесора;
- Може да се интегрира в клъстър;
- Използва се дългогодишно от големи [корпорации](https://www.rst.software/blog/22-companies-using-xmpp-and-ejabberd-to-build-instant-messaging-services)], което потвърждава стабилността му;
- Поддържа се от компанията [ProcessOne](https://www.process-one.net/), която има ясен механизъм за финансиране;
- **Conversation.im** използва **Ejabberd** и при разработката доставчикът се позовава на него вместо на **Prosody**.

Не ме разбирайте погрешно. Все още виждам в **Prosody** една прекрасна възможност за създаване на **XMPP** сървър. Дори все още поддържам и използвам един такъв. Безспорен факт е, че с него се работи изключително лесно.

* * *

## Предлагате ли други безплатни услуги?

Към момента на този домейн функционират услугите:

- [x] **XMPP**
- [ ] Електронна поща
- [ ] **Matrix** сървър
- [ ] **Nextcloud** сървър

!!! info "Информация"

    Само **XMPP** е публично достъпна услуга. Останалите за сега са в експериментална фаза. Ако все пак някоя от тях получи публичен достъп, това ще бъде анонсирано на уеб страницата. Също така ще забележете промяната в цвета на символа :fontawesome-regular-circle-check: пред съответната услуга от сив в зелен цвят.

!!! tip "Съвет"

    Моля, не изпращайте имейли или съобщения със запитвания относно дати и крайни срокове за публичен достъп до услуги различни от **XMPP**. На запитвания от този род **няма** да получите отговор.

## Планирате ли наличието на безплатен **Matrix** сървър с публичен достъп?

Към момента [**Matrix**](https://en.wikipedia.org/wiki/Matrix_(protocol)) функционира, но не е с публичен достъп. Поддръжката на тази платформа е доста по-сложна и трудоемка, съответно коства повече лично време. Също така изисква по-голям хардуерен и финансов ресурс. При всички случаи ще имам нужда от поне още един доброволец, с опит в **Linux** системната администрация, желаещ да инвестира **безвъзмездно** част от свободното си време в името на каузата.

* * *

## Планирате ли наличието на безплатна електронна поща с публичен достъп?

Към момента електронна поща функционира, но не е с публичен достъп. Поддръжката на такъв тип услуга е свързана със значително по-голяма отговорност към крайния потребител. От изключителна важност е денонощният мониторинг на системата с цел предотвратяване на инциденти свързани със сигурността. Сложна е за интеграция, но поддръжката е още по-сложна и трудоемка, съответно коства много повече лично време. Изисква голям хардуерен и финансов ресурс. При всички случаи ще имам нужда от поне още един или двама доброволци, с опит в **Linux** системната администрация, желаещи да инвестират **безвъзмездно** част от свободното си време в името на каузата.

* * *

## Планирате ли наличието на безплатен облак за съхранение на файлове с публичен достъп?

Към момента облак за съхранение на файлове функционира, но не е с публичен достъп. Поддръжката на такъв тип услуга е свързана с осигуряване на масив за съхранение на значителен обем данни. Отговорност към крайния потребител е сериозна част от това занимание. От изключителна важност е денонощният мониторинг на системата с цел предотвратяване на инциденти свързани със сигурността. Поддръжката е трудоемка, съответно коства много повече лично време. Изисква сериозна инвестиция в хардуер. При всички случаи ще имам нужда от поне още един или двама доброволци, с опит в **Linux** системната администрация, желаещи да инвестират **безвъзмездно** част от свободното си време в името на каузата.

* * *
## Има ли правила и условия за ползване на услугата?

Правилата за ползване на услугата са публикурани в раздел [Правила](https://docs.chatrix.one/terms/).

* * *

## Мога ли да подам сигнал за нарушение на правилата за ползване на услугата?

Вижте раздел [Правила](https://docs.chatrix.one/terms/) и по-точно частта [Подаване на сигнал](https://docs.chatrix.one/terms/#_3).

* * *

## Ще разберете ли, ако услугата стане недостъпна?

Услугата се мониторира денонощно по множество различни показатели. Освен това, лично аз я използвам ежедневно. В случай на проблем ще бъда известен в рамките на секунди. Следователно, не би трябвало да Ви се налага да се свързвате с мен за да ме уведомите, че нещо не е наред. Ще се погрижа проблемът да бъде отстранен възможно най-скоро.

!!! info "Информация"

    Отнасям се изключително сериозно към **непрекъснатостта на услугата**, но все пак имайте предвид, че имам семейство и лични ангажименти. Следователно, няма да ми бъде от полза, изпращането на куп съобщения или имейли с въпроси от типа: *Кога ще отстраните проблема?*

* * *

## Достъпна ли е услугата извън България?

Можете да използвате **Chatrix.One** от всяка точка на света. Към момента няма приложени [**GeoIP**](https://en.wikipedia.org/wiki/Geo-blocking) правила за блокиране на трафика.

* * *

## Къде мога да следя за настъпили инциденти?

Информация за настъпили инциденти, прекъсвания в услуката и предстоящи профилактики ще бъдат публикувани в раздел [Статус](https://docs.chatrix.one/status/#_4).

* * *

## Налична ли е техническа информация за услугата?

Проверете в раздел [Статус](https://docs.chatrix.one/status/#_2).

* * *

## Как мога да се свържа с вас?

Контактите са достъпни в долната част на страницата, както и в раздела [За Мен](https://docs.chatrix.one/about/#_2). Ако използвате мобилно устройство моля, проверете в менюто :material-menu:.