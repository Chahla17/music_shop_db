# База данных для магазина музыкальных инструментов.
Данная база данных содержит информацию о магазине музыкальных инструментов
# Типовые запросы к БД
-- 1. Найм сотрудника --

<pre style="color:#000000;background:#ffffff;"><span style="color:#800000; font-weight:bold; ">INSERT</span> <span style="color:#800000; font-weight:bold; ">INTO</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">music_shop</span><span style="color:#800000; ">`</span><span style="color:#808030; ">.</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">personal</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">(</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">full_name</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">positions_id</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">salary</span><span style="color:#800000; ">`</span><span style="color:#808030; ">)</span>
<span style="color:#800000; font-weight:bold; ">VALUES</span> <span style="color:#808030; ">(</span><span style="color:#0000e6; ">'Иван Иванов Иванович'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'2'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'20000'</span><span style="color:#808030; ">)</span><span style="color:#800080; ">;</span>
</pre>


-- 2. Увольнение сотрудника --

<pre style="color:#000000;background:#ffffff;"><span style="color:#800000; font-weight:bold; ">DELETE</span> <span style="color:#800000; font-weight:bold; ">FROM</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">personal</span><span style="color:#800000; ">`</span> <span style="color:#800000; font-weight:bold; ">WHERE</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">full_name</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">=</span> <span style="color:#0000e6; ">'Иван Иванов Сергеевич'</span><span style="color:#800080; ">;</span>
</pre>


-- 3. Добавить нового клиента --

<pre style="color:#000000;background:#ffffff;"><span style="color:#800000; font-weight:bold; ">INSERT</span> <span style="color:#800000; font-weight:bold; ">INTO</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">music_shop</span><span style="color:#800000; ">`</span><span style="color:#808030; ">.</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">clients</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">(</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">full_name</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">phone_number</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">email</span><span style="color:#800000; ">`</span><span style="color:#808030; ">)</span>
<span style="color:#800000; font-weight:bold; ">VALUES</span> <span style="color:#808030; ">(</span><span style="color:#0000e6; ">'Иван </span><span style="color:#0f69ff; "></span><span style="color:#0000e6; ">Другой </span>Виванович<span style="color:#0000e6; ">', '</span><span style="color:#808030; ">+</span><span style="color:#008c00; ">79999999998</span><span style="color:#0000e6; ">', '</span>ivan<span style="color:#797997; ">@gmail</span><span style="color:#808030; ">.</span>com<span style="color:#0000e6; ">');</span>
</pre>


-- 4. Добавить новый предмет на складе --

<pre style="color:#000000;background:#ffffff;"><span style="color:#800000; font-weight:bold; ">INSERT</span> <span style="color:#800000; font-weight:bold; ">INTO</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">music_shop</span><span style="color:#800000; ">`</span><span style="color:#808030; ">.</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">items</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">(</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">name</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">cost</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">types_id</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">number_of_items</span><span style="color:#800000; ">`</span><span style="color:#808030; ">)</span>
<span style="color:#800000; font-weight:bold; ">VALUES</span> <span style="color:#808030; ">(</span><span style="color:#0000e6; ">'Электрогитара'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'15000'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'3'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'5'</span><span style="color:#808030; ">)</span><span style="color:#800080; ">;</span>
</pre>

-- 5. Сделана покупка --

<pre style="color:#000000;background:#ffffff;"><span style="color:#800000; font-weight:bold; ">INSERT</span> <span style="color:#800000; ">INTO'music_shop</span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">`</span><span style="color:#808030; ">.</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">purchases</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">(</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">items_id</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">clients_id</span><span style="color:#800000; ">`</span><span style="color:#800080; ">,</span> <span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">personal_id</span><span style="color:#800000; ">`</span><span style="color:#808030; ">)</span>
<span style="color:#800000; font-weight:bold; ">VALUES</span> <span style="color:#808030; ">(</span><span style="color:#0000e6; ">'1'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'1'</span><span style="color:#800080; ">,</span> <span style="color:#0000e6; ">'2'</span><span style="color:#808030; ">)</span><span style="color:#800080; ">;</span>

<span style="color:#800000; font-weight:bold; "></span> <span style="color:#800000; ">UPDATE'music_shop</span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">`</span><span style="color:#808030; ">.</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">items'</span><span style="color:#800000; ">SET'</span>
<span style="color:#800000; font-weight:bold; "></span> <span style="color:#800000; ">number_of_items</span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">`</span> <span style="color:#808030; ">=</span> <span style="color:#808030; ">(</span><span style="color:#800000; font-weight:bold; ">SELECT'</span> <span style="color:#800000; "></span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">number_of_items'</span> <span style="color:#800000; font-weight:bold; "></span> <span style="color:#800000; ">FROM'</span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">items'</span> <span style="color:#800000; font-weight:bold; "></span> <span style="color:#800000; ">WHERE'</span><span style="color:#000000; background:#ffffff; "></span><span style="color:#800000; ">id`</span> <span style="color:#808030; ">=</span> <span style="color:#0000e6; ">'1'</span><span style="color:#808030; ">)</span> <span style="color:#808030; ">-</span> <span style="color:#008c00; "></span>
<span style="color:#800000; font-weight:bold; "></span> <span style="color:#808030; ">1WHERE(</span><span style="color:#800000; ">`</span><span style="color:#000000; background:#ffffff; ">id</span><span style="color:#800000; ">`</span> <span style="color:#808030; ">=</span> <span style="color:#0000e6; ">'1'</span><span style="color:#808030; ">)</span><span style="color:#800080; ">;</span>
</pre>

