Музикален магазин
=================
Да се напише програма за пазаруване на китари от музикален магазин.

В магазина има акустични и електрически китари. Акустичната китара се
характеризира със сила на звука (дробно число ватове). Електрическата китара се
характеризира с брой адаптри (pickups) и мощност на адаптрите (pickups output -
дробно число ватове).

Всяка китара в магазина има:
* брой струни (strings)
* брой прагчета (frets)
* тегло

Всеки музикален инструмент в магазина има:
* идентификационен номер
* цена
* марка

За музикалния магазин да се дефинират следните функционалности:
* `<колекция_от_китари> get_all_in_price_range(double from_price, double to_price) const` -
връща колекция от всички китари, чиято цена е в интервала [`from_price`,
`to_price`]
* `<колекция_от_китари> get_all_twelve_strings() const` - връща колекция от
всички дванадесет струнни китари
* `Acoustic const& get_most_powerful_acoustic() const` - връща акустична китара
с най-голяма сила на звука
* `Electric const& get_most_powerful_electric() const` - връща електрическа
китара с най-голяма мощност на адаптрите
* `void add_accoustic(Acoustic const& acoustic)` - добавя акустичната китара
`acoustic` в магазина
* `void add_electric(Electric const& electric)` - добавя електрическата китара
`electric` в магазина
* `void buy(Guitar const& guitar)` - купуване на китарата `guitar` от магазина

За всички класове да се дефинират подходящи конструктори и селектори.

Да се хвърлят подходящи изключения при:
* при опит за взимане на акустична китара с най-голяма сила на звука, когато
няма нито една акустична китара в магазина
* при опит за взимане на електрическа китара с най-голяма мощност на адаптрите,
когато няма нито една електрическа китара в магазина
* опит за добавяне на китара със същия идентификационен номер като на
съществуващ музикален инструмент в магазина
* опит за купуване на несъществуваща китара в магазина