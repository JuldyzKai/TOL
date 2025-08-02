< >
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Қыз Жібек жыры - Интерактивті тапсырмалар</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f5f5f5;
            margin: 0;
            padding: 20px;
            color: #333;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            background-color: rgb(243, 214, 253);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            padding: 20px;
        }
        h1 {
            color: #5a047f;
            text-align: center;
            margin-bottom: 30px;
        }
        .content-page p {
            text-indent: 1.5cm;  /* Бірінші жолдың кейін қоюы */
            margin-bottom: 1em;   /* Абзац аралығы */
            line-height: 1.6;     /* Жол аралығы */
            text-align: justify;  /* Екі жақты туралау */
            }
        .poem-with-image {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    margin: 8px 0;
}
.poem-image {
    flex: 0 0 auto;
    max-width: 200px;
}
.poem {
            flex: 1;
            white-space: pre-line;
            font-family: 'Times New Roman', serif;
            font-style: italic;
            line-height: 1.8;
            margin: 20px 0;
            padding: 15px;
            background-color: #f9f4ff;
            border-left: 4px solid #8e44ad;
            border-radius: 0 8px 8px 0;
            color: #5e3370;
            text-indent: 0;
        }
    
        .content-image {
            display: block;
            max-width: 60%;
            height: auto;
            margin: 20px auto;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            border: 1px solid #ddd;
        }
        .task-section {
            display: none;
            margin-bottom: 30px;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            background-color: #f9f9f9;
        }
        .active {
            display: block;
      
        }
        button {
            background-color: #8e44ad;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            margin: 5px;
            font-size: 16px;
        }
        button:hover {
            background-color: #732d91;
        }
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }
        .content-page {
            margin-bottom: 15px;
            padding: 10px;
            background-color: white;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .question {
            font-weight: bold;
            margin-bottom: 10px;
        }
        .dictionary-term {
            font-weight: bold;
            color: #8e44ad;
        }
        .drag-container {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-top: 15px;
        }
        .drag-item {
            padding: 10px;
            background-color: #e0e0e0;
            border-radius: 5px;
            cursor: move;
        }
        .drop-area {
            min-height: 100px;
            border: 2px dashed #8e44ad;
            border-radius: 5px;
            padding: 10px;
            margin-top: 10px;
        }
        .character-match {
            display: grid;
            grid-template-columns: 200px 1fr;
            gap: 15px;
            margin-top: 20px;
        }
        .match-row {
            display: flex;
            align-items: center;
            min-height: 60px;
        }
        .character {
            padding: 12px;
            background-color: #f0e6ff;
            border-radius: 8px;
            font-weight: bold;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .quote {
            padding: 12px;
            background-color: #e0f7fa;
            border-radius: 8px;
            cursor: move;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            margin-bottom: 10px;
        }
        .match-dropzone {
            min-height: 60px;
            border: 2px dashed #8e44ad;
            border-radius: 8px;
            padding: 10px;
            margin-left: 15px;
            background-color: rgba(142, 68, 173, 0.05);
        }
        .score-display {
            text-align: center;
            font-size: 24px;
            margin: 20px 0;
            padding: 15px;
            background-color: #8e44ad;
            color: white;
            border-radius: 8px;
        }
        .hint-btn {
            background-color: #f39c12;
            float: right;
        }
        .hint-btn:hover {
            background-color: #e67e22;
        }
        .shuffle-btn {
            background-color: #3498db;
            float: right;
        }
        .shuffle-btn:hover {
            background-color: #2980b9;
        }
        .correct {
            background-color: #2ecc71 !important;
            color: white;
        }
        .incorrect {
            background-color: #e74c3c !important;
            color: white;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 100;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.7);
        }
        .modal-content {
            background-color: #fefefe;
            margin: 10% auto;
            padding: 20px;
            border-radius: 10px;
            width: 80%;
            max-width: 600px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .close-btn {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }
        .close-btn:hover {
            color: black;
        }
        .task-image {
            text-align: center;
            margin: 15px 0;
        }
        .task-image img {
            max-width: 100%;
            max-height: 300px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        .poem {
            white-space: pre-line;
            font-family: 'Times New Roman', serif;
            font-style: italic;
            line-height: 1.8;
            margin: 20px 0;
            padding: 15px;
            background-color: #f9f4ff;
            border-left: 4px solid #8e44ad;
            border-radius: 0 8px 8px 0;
            color: #5e3370;
        }
        .match-game-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        .match-columns-container {
            display: flex;
            justify-content: space-between;
            gap: 20px;
            min-height: 400px;
        }
        .match-column {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
        }
        .match-column-title {
            background-color: #8e44ad;
            color: white;
            padding: 10px;
            border-radius: 5px;
            text-align: center;
            margin-bottom: 10px;
            font-weight: bold;
        }
        .match-items-container {
            flex: 1;
            background-color: rgba(255,255,255,0.7);
            border-radius: 8px;
            padding: 10px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            border: 2px dashed #8e44ad;
            min-height: 300px;
        }
        .match-item {
            background-color: white;
            border: 2px solid #8e44ad;
            border-radius: 8px;
            padding: 12px;
            cursor: grab;
            transition: all 0.3s ease;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            position: relative;
            user-select: none;
        }
        .match-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        .match-item.correct {
            background-color: #2ecc71;
            color: white;
            border-color: #2ecc71;
        }
        .match-item.incorrect {
            background-color: #e74c3c;
            color: white;
            border-color: #e74c3c;
        }
        .match-item.dragging {
            opacity: 0.8;
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0,0,0,0.3);
            z-index: 100;
        }
        .match-item.show-answer {
            background-color: #9b59b6;
            color: white;
            border-color: #9b59b6;
            box-shadow: 0 0 0 3px rgba(155, 89, 182, 0.5);
        }
        .match-controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        .match-feedback {
            text-align: center;
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            font-weight: bold;
            display: none;
        }
        .match-feedback.correct {
            background-color: rgba(46, 204, 113, 0.2);
            color: #2ecc71;
            display: block;
        }
        .match-feedback.incorrect {
            background-color: rgba(231, 76, 60, 0.2);
            color: #e74c3c;
            display: block;
        }
        @media (max-width: 768px) {
            .match-columns-container {
                flex-direction: column;
            }
            .match-column {
                width: 100%;
            }
        }
        
    </style>
</head>
<body>
    <div class="container">
        <h1>Қыз Жібек жыры</h1>

        <div id="task1" class="task-section active">
            <div class="content-page">
                <h3>Сансызбайдың шекті еліне сапары</h3>
                
                <p>Әлқисса, Сансызбай он жеті жасқа келді. Сегіз жылдай ағасынан хабар болмаған соң Төлегенді сағынып іздемекші болады. Қару-жарағын асынып атасына келіп, Төлегенді іздеуге рұқсат сұрады.
Сол күнде атасының көзі көр болып, көңілі жер болып, Төлегеннің қасіретінен санамен сарғайып, қайғыменен қарайып, тұрмастан жатады екен.
Сансызбайдың сөзін естіп зар жылап батасын береді.</p>

                <div class="poem">
– Бақытын ашқын баламның,
Жаратқан Алла бір Құдай,
Бір өзіңе аманат.
Разылық бермей жіберіп,
Төлегеннен айырылдым.
Жолың болсын, бар, балам,
Тапсырдым сені Аллаға.
Іздеп келгін ағаңды.
Атасы рұқсат берген соң,
Батасын алып Сансызбай,
Ер Шегені басшы қып,
Амандасып айырылып,
Қоштасып жұрты қалады.
Төлегенді іздеп Сансызбай
Сапарға басын салады.

                </div>

                <p>Әлқисса, Шеге мен Сансызбай бірнеше күн жол жүріп, Жайыққа келеді. Сырлыбайдың ауылын шарлап келе жатып бір белге шықса, бір ауылдың үстінде топырлаған көп атты адамды көреді.</p>
                <img src="Шеге мен төлеген.jpg" alt="Қазақ жыры" class="content-image">
            </div>
            <div class="content-page" style="display:none;">

                <h3>2</h3>
                <p>Бұл жиынның мән-жайын білейін деп анадайдан көрінген қойшыға келіп жолығады.
Қойшы айтты: «Бұл – Сырлыбай деген ханның ауылы. Сырлыбайдың Жібек деген асқан бір сұлу қызы бар еді. Жібектің сұлулығын естіген қалмақтың Қорен деген ханы тоғыз мың әскерімен шектінің үстін басып: «Жібекті қалыңдыққа бермесең, еліңді шабамын», – деді. Қалмаққа әлі келмейтін болған соң Сырлыбай Жібекті бермек болды. Сонда Жібек әкесіне арыз қылып: «Шынымен мені қалмаққа бермек болсаң, тым болмаса қырық күн тойын, отыз күн ойын қылып ұзат», – деді. Осы күні Жібектің тойы бітіп, ойынының басталғанына үш күн болды» – деді. «Жібек бұрын күйеуге берілген жоқ па еді?» – деп Шеге сұрады. Қойшы: «Жібектің Төлеген деген күйеуі бар еді. Қособаның көлі деген жерде оны Бекежен деген қарақшы өлтірді. Оған биыл сегіз жыл болды», – деді. Бұл сөзді естіген соң-ақ Сансызбай жылап жүре берді. Шеге Сансызбайдың артынан жүрді.</p>
               <div class="poem">
Сансызбай сонда жылады,
Көзінің жасын бұлады.
«Бауырың өлді», – деген соң,
Heшe мықты болса да,
Қайтіп шыдап тұрады.
«Артық туған көкешім,
Бұл дүниеден өтіпсің,
Шын дүниеге жетіпсің.
Қайран да менің көкешім,
Өлгеніңді есітіп,
Көзімнің жасын тыймадым».
</div>
<img src="Бекежан.jpg" alt="Жібек пен Төлегеннің кездесуі" class="content-image">
            </div>
            <div class="content-page" style="display:none;">
                 <h3>3</h3>
                <p>Жібек қыз әсемдігімен, ақылымен, шеберлігімен еліне танымал. Төлеген жігіт батырлығымен, шешендігімен көзге түседі. Екеуі бір-бірін көрген сәтте ғашық болады.</p>
                <div class="poem">
                <img src="Шеге.jpg" alt="Жібек пен Төлегеннің кездесуі" class="content-image"> 
– Айналайын Сансызбай,
Көлге біткен құрағым,
Суырылып озған пырағым.
Жасын тыйғын көзіңнің,
Жыламағын, шырағым.
Рас болса өлгені
Төлеген сынды ағаңның,
Ұжмақтан жазсын тұрағын.
</div>

<p>Сонда Сансызбай айтты: «Жібекті қолымыздан келсе алып кетелік, қолымыздан келмесе жүзін көріп, жолығып кетелік. Сіз Жібекті тауып, күй-жайын біліп келіңіз?» – деп. Екеуі Сырлыбайдың ауылына қарай жүрді. Жиылған көпке жақын келді. Сонда Сансызбай: «Жиылған тамашаны өзім барып көріп, барлап біліп келейін» – деді де, атын Шегеге беріп, өзі жаяу топтың ішіне кіріп кетті. Ойынды тамашалап аралап жүрсе, бір үлкен үйден зарлаған дауыс естіді. Үйдің қасына барса мынадай зар екен:</p>
 <div class="poem">
 Жібектің зары:
– Жайықтың суы ылай-ай,
Көр болды көзім жылай-ай.
Төлеген сынды мырзадан
Айырдың өзің, Құдай-ай.
</div>

            </div>
            <div class="content-page" style="display:none;">
                 <h3>4</h3>
                <p>Әлқисса, Сансызбай зарлап отырған әйелдің Жібек екенін таныды да, қайтадан жүгіріп Шегеге келіп, Жібектен бір жауап алып бер деп айтқаны:</p>
                <div class="poem">
«Айналайын Шеге аға,
Жібек сынды жеңгеме
Жұмсадым сізді мен, аға.
Жалғыз-ақ арыз сөзім бар,
Қыз Жібектей жеңгемнен
Бір жауап әкеп бер, аға!»
Батыр туған Шеге ақын,
Өлең айтқан ақ үйдің
Тұсына таман келеді.
</div>
<p>Әлқисса, қалың қолды аралап, үлкен ақ үйге Шеге жақындап келсе, үйдің ішінен зарлаған дауыс естіпті. Құлағын салып тыңдаса, мына сөзді айтып зарлаған Жібек екен:</p>
                <div class="poem">
«Әуелі бас қосқаным жағалбайлы,
Жылқысын көптігінен баға алмайды.
Өлгені Төлегеннің рас болса,
Құдайым Қыз Жібекті неге алмайды?
Сол елде сері жігіт жоқ па, Тәңірі-ай,
Жесірін іздеп келіп неге алмайды?»
</div>
<img src="Ж пен Т.jpg" alt="Жібек пен Төлегеннің кездесуі" class="content-image">
            </div>
            <div class="content-page" style="display:none;">
                 <h3>Шеге мен Жібектің айтысқаны</h3>
                <p>Әлқисса, Шеге Жібектің тұсына жақындап келеді. Мұңды болып отырған Жібекті көреді. Жігіт болып өлең айтып, Жібекпен таныспақшы болады. </p>
        <div class="poem">          
Шеге ақын:
   – Естіп ем осы тойды сіздікі деп,
   Жарқыным, не себептен болдың мұңлы?
Жібек:
   – Көргендей жол бейнетін жүзің сарық,
   Тұсыма қалың топты келдің жарып.
   Торға түскен тұйғындай пенде болып,
   Айырылған ел-жұртынан мен бір ғаріп.
Шегенің сөзі:
   – Бітіпті хор қызындай саған көрік,
   Сүйегім әр сөзіңе барады еріп.
   Жарқыным, қалайша боп түстің торға?
   Мәнісін айтыңызшы, есітелік.
Жібек:
   – Алланың үкіміне жүрмін көніп,
   Зар болдым жаққан шырақ отым сөніп.
   Құдайым айырған соң қосағымнан,
   Отырмын жау қалмаққа пенде болып.
Шегенің сауалы:
   – Қайын ата, қайын анаң қай рудан,
   Есімі күйеуіңнің кім болады?
</div>
<img src="Шеге мен Жібек.jpg" alt="Жібек пен Шегенің кездесуі" class="content-image">
            </div>
            <div class="content-page" style="display:none;">
                 <h3>6</h3>
                <div class="poem">
Жібек:
   – Қайын атам аты – Базарбай
   Жағалбайлы – руы.
   Төлеген – оның баласы,
   Ілгері еді патшадан
   Ақылының данасы.
   Қайран да Тәңірім, қайтейін,
   Болмады аз күн жүруі.
   Қайын енем атын айтайын
   Алпыс жасар Қамқадай.
   Тірі болса Сансызбай
   Ержетер уақыты боп еді.
   Біздей ғаріп міскінді
   Неге бір іздеп келмейді?
   «Елімнің ақын көсемі
   Батыр Шеге», – деп еді.
Сонда Шеге сөйлейді:
    – Сансызбайға басшы боп,
   Іздеп келген өзіңді
   Ақын Шегең мен, – дейді.
   Әккі болған Қыз Жібек:
   «Алдап жүрген біреу», – деп, 
   Бұл сөзіне сенбейді.
Сонда Жібек сөйледі:
   – Шын айтқан болсаң, әй, аға,
   Соңыңда жүріп өлейін.
</div>
<img src="А мен Т.jpg" alt="Жібек пен Төлегеннің кездесуі" class="content-image">
            </div>
            <div class="content-page" style="display:none;">
                <h3>7</h3>
                <div class="poem">
Сансызбай қайда, көрсетші?
Айналайын ағажан,
Сөзіңе сонда сенейін.
«Жалғыз қайның келді», – деп,
Батыр туған Шеге ақын,
Жібекке хабар береді.
– Алтыннан соққан қияғым,
Күмістен соққан тұяғым,
Құдай қалай ұқсатқан
Көкесіне сыяғын.
Жаратқан Алла жар болып,
Жанды ғой өшкен шырағым.
Ашылсаңшы, қабағым,
Өлгенім тіріліп келіп тұр,
Жарылсаңшы, жүрегім.
– Мені алғалы кеп жатқан жау қалмақтың
Екі тұлпар аты бар, білгін, – дейді.
Қара ағаш кезеңінен жол асады,
Сол жолда мені тосып тұрғын, – дейді.
Құдай оңдап, тұлпардың мінсем бірін,
Ертең түсте сол жерде көргін, – дейді.
Біздің ел ертең тұра көшер деймін,
Түннен-ақ үйдің бауын шешер деймін.
Құдай біздің тілекті берсе егер,
Шырағы жау қалмақтың өшер деймін.
</div>
<img src="Қалыңд.jpg" alt="Жібектің қашып кетуі" class="content-image">
            </div>
            <button onclick="nextPage(1)">Келесі бет</button>
        </div>
        
       <div id="task2" class="task-section">
            <div class="task-image">
<img src="ҚызЖ.jpg" alt="Тарихи сурет">
            </div>

            
            <h2>2. Біліп ал</h2>
            <p>Жібек жырындағы маңызды оқиғалар мен фактілер:</p>
            <ul>
                <li>Жыр XV-XVI ғасырларда пайда болған</li>
                <li>Қыз Жібек - лирикалық-эпикалық жыр</li>
                <li>Негізгі тақырыбы - махаббат пен адалдық</li>
                <li>Жырда қазақтың дәстүрлі тұрмысы, салт-дәстүрі көрініс тапқан</li>
            </ul>
            <div class="question">
                <p>Жібек жыры қандай ғасырда пайда болған?</p>
                <button onclick="checkAnswer(this, true)">XV-XVI ғасырларда</button>
                <button onclick="checkAnswer(this, false)">XII-XIII ғасырларда</button>
                <button onclick="checkAnswer(this, false)">XVIII ғасырда</button>
            </div>
            <button class="hint-btn" onclick="showHint(2)">Кілт</button>
        </div>
        
        <div id="task3" class="task-section">
            <div class="task-image">
                <img src="БТ.jpg" alt="Кейіпкерлер">
            </div>
            <h2>3. Сауал</h2>
            <div class="question">
                <p>Жібек қыздың ерекше қасиеттері қандай?</p>
                <button onclick="checkAnswer(this, true)">Әсемдігі, ақылы, шеберлігі</button>
                <button onclick="checkAnswer(this, false)">Батырлығы, ерлігі</button>
                <button onclick="checkAnswer(this, false)">Байлығы, ықпалы</button>
            </div>
            <div class="question">
                <p>Төлеген жігіттің қандай қасиеттері бар?</p>
                <button onclick="checkAnswer(this, true)">Батырлығы, шешендігі</button>
                <button onclick="checkAnswer(this, false)">Шеберлігі, әдемілігі</button>
                <button onclick="checkAnswer(this, false)">Байлығы, билігі</button>
            </div>
            <div class="question">
                <p>Жібек пен Төлегеннің арасында не болды?</p>
                <button onclick="checkAnswer(this, true)">Олар бір-бірін көрген сәтте ғашық болды</button>
                <button onclick="checkAnswer(this, false)">Олар бірге өскен</button>
                <button onclick="checkAnswer(this, false)">Оларды ата-аналары үйлендірді</button>
            </div>
            <button class="hint-btn" onclick="showHint(3)">Кілт</button>
            <button class="shuffle-btn" onclick="shuffleAnswers(3)">Араластыру</button>
        </div>
        
        <div id="task4" class="task-section">
            <div class="task-image">
                <img src="Жібек пен Т.jpg" alt="Сөздік">
            </div>
            <h2>4. Сөздік</h2>
            <p><span class="dictionary-term">Жыр</span> - поэзиялық шығарма, әдебиеттің өлеңмен жазылатын түрі.</p>
            <p><span class="dictionary-term">Лирикалық</span> - сезім, эмоция, ішкі әлемді бейнелейтін.</p>
            <p><span class="dictionary-term">Эпикалық</span> - оқиғаны, тарихи құбылысты баяндайтын.</p>
            <p><span class="dictionary-term">Махаббат</span> - адамдар арасындағы қуатты жанашырлық сезімі.</p>
            <div class="question">
                <p>"Эпикалық" сөзінің мағынасы қандай?</p>
                <button onclick="checkAnswer(this, true)">Оқиғаны, тарихи құбылысты баяндайтын</button>
                <button onclick="checkAnswer(this, false)">Сезім, эмоцияны бейнелейтін</button>
                <button onclick="checkAnswer(this, false)">Күлкілі, әзілді шығарма</button>
            </div>
            <button class="hint-btn" onclick="showHint(4)">Кілт</button>
        </div>
        
        <div id="task5" class="task-section">
    <div class="task-image">
        <img src="ҚызЖ.jpg" alt="Оқиғалар">
    </div>
    <h2>5. Тірек сөздер</h2>
    <p>Төмендегі сөздерді қолданып, Жібек жыры туралы қысқаша шығарма жазыңыз:</p>
    <div class="drag-container">
        <div class="drag-item" draggable="true" ondragstart="drag(event)">махаббат</div>
        <div class="drag-item" draggable="true" ondragstart="drag(event)">қиыншылық</div>
        <div class="drag-item" draggable="true" ondragstart="drag(event)">адалдық</div>
        <div class="drag-item" draggable="true" ondragstart="drag(event)">кедергі</div>
        <div class="drag-item" draggable="true" ondragstart="drag(event)">жыр</div>
    </div>
    <p>Мәтінді жазыңыз:</p>
   
    <textarea id="text-input" style="width: 100%; min-height: 100px; margin-top: 10px;" 
              placeholder="Мәтінді осы жерге жазыңыз "></textarea>
    
</div>
            
        <div id="task6" class="task-section">
            <div class="task-image">
                <img src="ҚызЖ.jpg" alt="Оқиғалар">
            </div>
            
            <h3 style="margin-top: 30px;">6. Оқиғаларды ретімен орналастыр</h3>
            <div class="drag-container" id="events-sequence">
                <div class="drag-item" draggable="true" ondragstart="drag(event)">Жібек пен Төлегеннің кездесуі</div>
                <div class="drag-item" draggable="true" ondragstart="drag(event)">Жібектің қашып кетуі</div>
                <div class="drag-item" draggable="true" ondragstart="drag(event)">Төлегеннің Жібекті іздеуі</div>
                <div class="drag-item" draggable="true" ondragstart="drag(event)">Жібектің қайтуы</div>
            </div>
            <p>Дұрыс ретті құрастырыңыз:</p>
            
            <textarea id="text-input" style="width: 100%; min-height: 100px; margin-top: 10px;" 
              placeholder="Мәтінді осы жерге жазыңыз "></textarea>
            <button onclick="checkSequence()">Тексеру</button>
            <button class="hint-btn" onclick="showHint(5)">Кілт</button>
            <button class="shuffle-btn" onclick="shuffleEvents()">Араластыру</button>
        </div>
        <div id="task7" class="task-section">
            <div class="task-image">
                <img src="Бекежан.jpg" alt="Кейіпкерлер сөздері">
            </div>
            <h2>7. Кейіпкерлер сөздерін сәйкестендіру</h2>
            <p>Кейіпкерлерді олардың сөздерімен сәйкестендіріңіз:</p>
            
            <div class="match-game-container">
                <div class="match-columns-container">
                    <div class="match-column">
                        <div class="match-column-title">Кейіпкерлер</div>
                        <div class="match-items-container" id="characters-column">
                            <!-- Кейіпкерлер мұнда қосылады -->
                        </div>
                    </div>
                    
                    <div class="match-column">
                        <div class="match-column-title">Сөздер</div>
                        <div class="match-items-container" id="quotes-column">
                            <!-- Сөздер мұнда қосылады -->
                        </div>
                    </div>
                </div>
                
                <div class="match-controls">
                    <button onclick="checkMatches()">Тексеру</button>
                    <button onclick="resetMatches()">Қалпына келтіру</button>
                    <button class="hint-btn" onclick="showHint(6)">Кілт</button>
                    <button class="shuffle-btn" onclick="shuffleMatches()">Араластыру</button>
                </div>
                
                <div class="match-feedback" id="match-feedback"></div>
            </div>
        </div>
        
        <div id="task7" class="task-section">
            <div class="task-image">
                <img src="Шеге.jpg" alt="Нәтижелер">
            </div>
            <h2>7. Нәтижелер</h2>
            <div class="score-display">
                Сіз жинаған ұпай: <span id="total-score">0</span>
            </div>
            <div id="mistakes-list" style="margin-top: 20px;">
                <h3>Қателер:</h3>
                <ul id="mistakes">
                    <!-- Қателер мұнда көрсетіледі -->
                </ul>
            </div>
            <button onclick="showAllHints()">Барлық дұрыс жауаптарды көрсету</button>
        </div>
        
        <div class="navigation">
            <button id="prev-btn" onclick="prevTask()">Алдыңғы</button>
            <button id="next-btn" onclick="nextTask()">Келесі</button>
        </div>
    </div>

    <!-- Кілт үшін модальды терезе -->
    <div id="hintModal" class="modal">
        <div class="modal-content">
            <span class="close-btn" onclick="closeModal()">&times;</span>
            <h3 id="modalTitle">Кілт ақпараты</h3>
            <div id="modalContent"></div>
        </div>
    </div>

    <script>
        let currentTask = 1;
        const totalTasks = 7;
        let score = 0;
        let mistakes = [];
        const correctSequence = [
            "Жібек пен Төлегеннің кездесуі",
            "Жібектің қашып кетуі",
            "Төлегеннің Жібекті іздеуі",
            "Жібектің қайтуы"
        ];
        
        // Сәйкестендіру ойыны үшін деректер
        const matchData = [
            { character: "Жібек", quote: "\"Құдайым-ай, құдайым-ай, қайда барасың?\"" },
            { character: "Төлеген", quote: "\"Жібек деген қыз бар екен, көргенге тұрар қыз бар екен\"" },
            { character: "Бекежан", quote: "\"Төлеген деген жігіт бар екен, көргенге тұрар жігіт бар екен\"" }
        ];
        
        let draggedMatchItem = null;
        
        function showTask(taskNumber) {
            document.querySelectorAll('.task-section').forEach(section => {
                section.classList.remove('active');
            });
            document.getElementById(`task${taskNumber}`).classList.add('active');
            currentTask = taskNumber;
            
            document.getElementById('prev-btn').style.display = taskNumber === 1 ? 'none' : 'block';
            document.getElementById('next-btn').style.display = taskNumber === totalTasks ? 'none' : 'block';
            
            // 6-тапсырманы көрсеткенде ойынды бастау
            if (taskNumber === 6) {
                initMatchGame();
            }
        }

        function nextTask() {
            if (currentTask < totalTasks) {
                showTask(currentTask + 1);
            }
        }

        function prevTask() {
            if (currentTask > 1) {
                showTask(currentTask - 1);
            }
        }

        function nextPage(taskNumber) {
            const pages = document.querySelectorAll(`#task${taskNumber} .content-page`);
            let foundCurrent = false;
            
            for (let i = 0; i < pages.length; i++) {
                if (pages[i].style.display !== 'none' && !foundCurrent) {
                    pages[i].style.display = 'none';
                    foundCurrent = true;
                    if (i + 1 < pages.length) {
                        pages[i + 1].style.display = 'block';
                    } else {
                        pages[0].style.display = 'block';
                    }
                    break;
                }
            }
        }

        function checkAnswer(button, isCorrect) {
            const buttons = button.parentNode.querySelectorAll('button');
            buttons.forEach(btn => {
                btn.classList.remove('correct', 'incorrect');
                btn.disabled = true;
            });
            
            if (isCorrect) {
                button.classList.add('correct');
                score += 10;
            } else {
                button.classList.add('incorrect');
                const questionText = button.parentNode.querySelector('p').textContent;
                const correctAnswer = Array.from(buttons).find(btn => btn.onclick.toString().includes('true')).textContent;
                mistakes.push({question: questionText, correctAnswer: correctAnswer});
            }
            
            updateScore();
        }

        function showHint(taskNumber) {
            const modal = document.getElementById('hintModal');
            const title = document.getElementById('modalTitle');
            const content = document.getElementById('modalContent');
            
            title.textContent = `${taskNumber}-тапсырма үшін кілт`;
            
            switch(taskNumber) {
                case 1:
                    content.innerHTML = `
                        <p><strong>Қыз Жібек жыры</strong> - қазақ халқының ең көрнекі лирикалық жырларының бірі.</p>
                        <p>Жырда Жібек пен Төлегеннің махаббаты, олардың арасындағы кедергілер, қиыншылықтар баяндалады.</p>
                    `;
                    break;
                case 2:
                    content.innerHTML = `
                        <p><strong>Жібек жырының негізгі фактілері:</strong></p>
                        <ul>
                            <li>Жыр <strong>XV-XVI ғасырларда</strong> пайда болған</li>
                            <li>Қыз Жібек - <strong>лирикалық-эпикалық жыр</strong></li>
                            <li>Негізгі тақырыбы - <strong>махаббат пен адалдық</strong></li>
                        </ul>
                    `;
                    break;
                case 3:
                    content.innerHTML = `
                        <p><strong>Дұрыс жауаптар:</strong></p>
                        <ul>
                            <li><strong>Жібек қыздың ерекше қасиеттері:</strong> әсемдігі, ақылы, шеберлігі</li>
                            <li><strong>Төлеген жігіттің қасиеттері:</strong> батырлығы, шешендігі</li>
                            <li><strong>Жібек пен Төлегеннің арасында:</strong> олар бір-бірін көрген сәтте ғашық болды</li>
                        </ul>
                    `;
                    break;
                case 4:
                    content.innerHTML = `
                        <p><strong>Сөздіктегі терминдер:</strong></p>
                        <ul>
                            <li><strong>Жыр</strong> - поэзиялық шығарма, әдебиеттің өлеңмен жазылатын түрі</li>
                            <li><strong>Лирикалық</strong> - сезім, эмоция, ішкі әлемді бейнелейтін</li>
                            <li><strong>Эпикалық</strong> - оқиғаны, тарихи құбылысты баяндайтын</li>
                            <li><strong>Махаббат</strong> - адамдар арасындағы қуатты жанашырлық сезімі</li>
                        </ul>
                    `;
                    break;
                case 5:
                    content.innerHTML = `
                        <p><strong>Оқиғалардың дұрыс реті:</strong></p>
                        <ol>
                            <li>Жібек пен Төлегеннің кездесуі</li>
                            <li>Жібектің қашып кетуі</li>
                            <li>Төлегеннің Жібекті іздеуі</li>
                            <li>Жібектің қайтуы</li>
                        </ol>
                    `;
                    break;
                case 6:
                    content.innerHTML = `
                        <p><strong>Кейіпкерлер мен сөздердің дұрыс сәйкестендіруі:</strong></p>
                        <ul>
                            <li><strong>Жібек:</strong> "Құдайым-ай, құдайым-ай, қайда барасың?"</li>
                            <li><strong>Төлеген:</strong> "Жібек деген қыз бар екен, көргенге тұрар қыз бар екен"</li>
                            <li><strong>Бекежан:</strong> "Төлеген деген жігіт бар екен, көргенге тұрар жігіт бар екен"</li>
                        </ul>
                    `;
                    break;
                case 7:
                    content.innerHTML = `<p>Тапсырмаларды орындау барысында жинаған ұпайларыңызды және қателерді қарап шығуға болады.</p>`;
                    break;
                default:
                    content.textContent = "Кілт ақпараты";
            }
            
            modal.style.display = "block";
        }

        function closeModal() {
            document.getElementById('hintModal').style.display = "none";
        }

        function showAllHints() {
            const modal = document.getElementById('hintModal');
            const title = document.getElementById('modalTitle');
            const content = document.getElementById('modalContent');
            
            title.textContent = "Барлық тапсырмаларға кілттер";
            
            let allHints = `
                <div style="max-height: 400px; overflow-y: auto;">
                    <h4>1-тапсырма: Мазмұн</h4>
                    <p>Қыз Жібек - қазақ халқының ең көрнекі лирикалық жырларының бірі. Жырда Жібек пен Төлегеннің махаббаты, олардың арасындағы кедергілер, қиыншылықтар баяндалады.</p>
                    
                    <h4>2-тапсырма: Біліп ал</h4>
                    <ul>
                        <li>Жыр <strong>XV-XVI ғасырларда</strong> пайда болған</li>
                        <li>Қыз Жібек - <strong>лирикалық-эпикалық жыр</strong></li>
                        <li>Негізгі тақырыбы - <strong>махаббат пен адалдық</strong></li>
                    </ul>
                    
                    <h4>3-тапсырма: Сауал</h4>
                    <ul>
                        <li>Жібек қыздың ерекше қасиеттері: <strong>әсемдігі, ақылы, шеберлігі</strong></li>
                        <li>Төлеген жігіттің қасиеттері: <strong>батырлығы, шешендігі</strong></li>
                        <li>Жібек пен Төлегеннің арасында: <strong>олар бір-бірін көрген сәтте ғашық болды</strong></li>
                    </ul>
                    
                    <h4>4-тапсырма: Сөздік</h4>
                    <ul>
                        <li><strong>Эпикалық</strong> - оқиғаны, тарихи құбылысты баяндайтын</li>
                    </ul>
                    
                    <h4>5-тапсырма: Тірек сөздер</h4>
                    <p><strong>Оқиғалардың дұрыс реті:</strong></p>
                    <ol>
                        <li>Жібек пен Төлегеннің кездесуі</li>
                        <li>Жібектің қашып кетуі</li>
                        <li>Төлегеннің Жібекті іздеуі</li>
                        <li>Жібектің қайтуы</li>
                    </ol>
                    
                    <h4>6-тапсырма: Кейіпкерлер сөздерін сәйкестендіру</h4>
                    <ul>
                        <li><strong>Жібек:</strong> "Құдайым-ай, құдайым-ай, қайда барасың?"</li>
                        <li><strong>Төлеген:</strong> "Жібек деген қыз бар екен, көргенге тұрар қыз бар екен"</li>
                        <li><strong>Бекежан:</strong> "Төлеген деген жігіт бар екен, көргенге тұрар жігіт бар екен"</li>
                    </ul>
                </div>
            `;
            
            content.innerHTML = allHints;
            modal.style.display = "block";
        }

        function shuffleAnswers(taskNumber) {
            const container = document.querySelector(`#task${taskNumber}`);
            const questions = container.querySelectorAll('.question');
            
            questions.forEach(question => {
                const buttons = Array.from(question.querySelectorAll('button'));
                for (let i = buttons.length - 1; i > 0; i--) {
                    const j = Math.floor(Math.random() * (i + 1));
                    question.insertBefore(buttons[j], buttons[i]);
                }
            });
        }

        function allowDrop(ev) {
            ev.preventDefault();
        }

        function drag(ev) {
            ev.dataTransfer.setData("text", ev.target.id);
        }

        function drop(ev) {
            ev.preventDefault();
            const data = ev.dataTransfer.getData("text");
            const draggedElement = document.getElementById(data);
            
            if (draggedElement.parentNode !== ev.target) {
                ev.target.appendChild(draggedElement);
            }
        }

        function dropSequence(ev) {
            ev.preventDefault();
            const data = ev.dataTransfer.getData("text");
            const draggedElement = document.getElementById(data);
            
            while (ev.target.firstChild) {
                document.getElementById('events-sequence').appendChild(ev.target.firstChild);
            }
            
            ev.target.appendChild(draggedElement);
        }

        function checkSequence() {
            const dropArea = document.getElementById('sequence-drop');
            const items = dropArea.querySelectorAll('.drag-item');
            let allCorrect = true;
            
            items.forEach((item, index) => {
                if (item.textContent === correctSequence[index]) {
                    item.classList.add('correct');
                    item.classList.remove('incorrect');
                } else {
                    item.classList.add('incorrect');
                    item.classList.remove('correct');
                    allCorrect = false;
                }
            });
            
            if (allCorrect && items.length === correctSequence.length) {
                score += 20;
                updateScore();
                alert("Дұрыс! Сіз оқиғаларды дұрыс ретпен орналастырдыңыз!");
            } else {
                mistakes.push({question: "Оқиғаларды ретімен орналастыру", correctAnswer: correctSequence.join(", ")});
                updateScore();
            }
        }

        function shuffleEvents() {
            const container = document.getElementById('events-sequence');
            const items = Array.from(container.querySelectorAll('.drag-item'));
            
            for (let i = items.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                container.appendChild(items[j]);
            }
        }

        // Сәйкестендіру ойынын бастау
        function initMatchGame() {
            const charactersColumn = document.getElementById('characters-column');
            const quotesColumn = document.getElementById('quotes-column');
            
            // Бос ету
            charactersColumn.innerHTML = '';
            quotesColumn.innerHTML = '';
            
            // Кейіпкерлерді қосу
            matchData.forEach(item => {
                const charElement = createMatchItem(item.character, 'character');
                charactersColumn.appendChild(charElement);
            });
            
            // Сөздерді араластырып қосу
            const shuffledQuotes = [...matchData].sort(() => Math.random() - 0.5);
            shuffledQuotes.forEach(item => {
                const quoteElement = createMatchItem(item.quote, 'quote');
                quotesColumn.appendChild(quoteElement);
            });
            
            // Feedback жасыру
            document.getElementById('match-feedback').style.display = 'none';
            
            // Drag and drop қосу
            setupMatchDragAndDrop();
        }
        
        // Сәйкестендіру элементін жасау
        function createMatchItem(text, type) {
            const element = document.createElement('div');
            element.className = 'match-item';
            element.textContent = text;
            element.dataset.type = type;
            element.draggable = true;
            
            // Типке байланысты стиль
            if (type === 'character') {
                element.style.backgroundColor = '#f0e6ff';
            } else {
                element.style.backgroundColor = '#e0f7fa';
            }
            
            return element;
        }
        
        // Drag and drop орнату
        function setupMatchDragAndDrop() {
            const items = document.querySelectorAll('.match-item');
            const containers = document.querySelectorAll('.match-items-container');
            
            items.forEach(item => {
                item.addEventListener('dragstart', (e) => {
                    draggedMatchItem = item;
                    setTimeout(() => {
                        item.classList.add('dragging');
                    }, 0);
                    e.dataTransfer.setData('text/plain', '');
                });
                
                item.addEventListener('dragend', () => {
                    item.classList.remove('dragging');
                    draggedMatchItem = null;
                });
            });
            
            containers.forEach(container => {
                container.addEventListener('dragover', (e) => {
                    e.preventDefault();
                    const afterElement = getMatchDragAfterElement(container, e.clientY);
                    const dragging = document.querySelector('.match-item.dragging');
                    
                    if (afterElement == null) {
                        container.appendChild(dragging);
                    } else {
                        container.insertBefore(dragging, afterElement);
                    }
                });
            });
        }
        
        // Drag позициясын анықтау
        function getMatchDragAfterElement(container, y) {
            const draggableElements = [...container.querySelectorAll('.match-item:not(.dragging)')];
            
            return draggableElements.reduce((closest, child) => {
                const box = child.getBoundingClientRect();
                const offset = y - box.top - box.height / 2;
                
                if (offset < 0 && offset > closest.offset) {
                    return { offset: offset, element: child };
                } else {
                    return closest;
                }
            }, { offset: Number.NEGATIVE_INFINITY }).element;
        }
        
        // Сәйкестендіруді тексеру
        function checkMatches() {
            const charactersColumn = document.getElementById('characters-column');
            const quotesColumn = document.getElementById('quotes-column');
            const feedback = document.getElementById('match-feedback');
            
            const characterItems = Array.from(charactersColumn.children);
            const quoteItems = Array.from(quotesColumn.children);
            
            let allCorrect = true;
            
            characterItems.forEach((charItem, index) => {
                const charText = charItem.textContent;
                const quoteText = quoteItems[index]?.textContent || '';
                
                // Дұрыс жұпты табу
                const correctPair = matchData.find(item => 
                    item.character === charText && item.quote === quoteText
                );
                
                if (correctPair) {
                    charItem.classList.add('correct');
                    charItem.classList.remove('incorrect');
                    if (quoteItems[index]) {
                        quoteItems[index].classList.add('correct');
                        quoteItems[index].classList.remove('incorrect');
                    }
                } else {
                    charItem.classList.add('incorrect');
                    charItem.classList.remove('correct');
                    if (quoteItems[index]) {
                        quoteItems[index].classList.add('incorrect');
                        quoteItems[index].classList.remove('correct');
                    }
                    allCorrect = false;
                }
            });
            
            // Feedback көрсету
            if (allCorrect) {
                feedback.textContent = 'Керемет! Барлық жауаптар дұрыс!';
                feedback.className = 'match-feedback correct';
                score += 30;
                updateScore();
            } else {
                feedback.textContent = 'Кейбір жауаптар қате. Қайталап көріңіз!';
                feedback.className = 'match-feedback incorrect';
            }
            
            feedback.style.display = 'block';
        }
        
        // Сәйкестендіруді қалпына келтіру
        function resetMatches() {
            initMatchGame();
        }
        
        // Сәйкестендіруді араластыру
        function shuffleMatches() {
            const quotesColumn = document.getElementById('quotes-column');
            const quoteItems = Array.from(quotesColumn.children);
            
            // Араластыру
            for (let i = quoteItems.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                quotesColumn.insertBefore(quoteItems[j], quoteItems[i]);
            }
            
            // Стильдерді қалпына келтіру
            quoteItems.forEach(item => {
                item.classList.remove('correct', 'incorrect');
            });
            
            document.getElementById('match-feedback').style.display = 'none';
        }

        function updateScore() {
            document.getElementById('total-score').textContent = score;
            
            const mistakesList = document.getElementById('mistakes');
            mistakesList.innerHTML = '';
            
            mistakes.forEach(mistake => {
                const li = document.createElement('li');
                li.innerHTML = `<strong>${mistake.question}</strong><br>Дұрыс жауап: ${mistake.correctAnswer}`;
                mistakesList.appendChild(li);
            });
        }

        // Модальды терезенің сыртын басқанда жабу
        window.onclick = function(event) {
            const modal = document.getElementById('hintModal');
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }
        
        // DOM жүктегенде сәйкестендіру ойынын бастау
        document.addEventListener('DOMContentLoaded', () => {
            initMatchGame();
        });
    </script>
</body>
</html>
