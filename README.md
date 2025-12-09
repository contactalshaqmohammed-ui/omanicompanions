
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>عرض الصحابة العمانيين</title>
    <style>
        body {
        font-family: Arial, sans-serif;
        background: linear-gradient(135deg, #e8fce8, #ffffff, #e8fce8);
        background-size: 400% 400%;
        animation: softMove 12s ease-in-out infinite;
        padding: 20px;
    }
        h1, h2 {
            text-align: center;
        }
        h1 {
            color: #008000;
            font-size: 2.5em;
            margin-top: 15px;
            margin-bottom: 5px;
            text-shadow: 1px 1px 2px rgba(255, 255, 255, 0.7);
        }
        h2 {
            color: #555;
            font-size: 1.2em;
            margin-bottom: 30px;
        }
        .logos {
            text-align: center;
            margin-bottom: 25px;
            border-bottom: 1px solid #ddd;
            padding-bottom: 15px;
        }
        .logos img {
            height: 90px;
            margin: 0 15px;
            max-width: 40%;
            object-fit: contain;
        }
        .characters-wrapper {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 20px auto;
            max-width: 850px;
        }
        .character-column {
            display: flex;
            flex-direction: column;
            gap: 15px;
            width: 100%;
            max-width: 380px;
        }
        @media (min-width: 768px) {
            .character-column {
                width: calc(50% - 15px);
            }
        }
        .character {
        background: white;
        padding: 15px;
        border-radius: 12px;
        text-align: center;
        cursor: pointer;
        box-shadow: 0 2px 5px rgba(0,0,0,0.15);
        transition: transform 0.3s ease, box-shadow 0.3s ease, background-color 0.3s;
        position: relative;
        overflow: hidden;
    }
        .character:hover {
        transform: translateY(-6px) scale(1.06);
        box-shadow: 0 8px 20px rgba(0,0,0,0.25);
        background-color: #eaffea;
    }
        #detailsBox {
            margin: 50px auto 20px;
            background: rgba(233, 245, 233, 0.95);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
            display: none;
            border: 2px solid #008000;
            max-width: 800px;
            text-align: right;
            line-height: 1.8;
            font-size: 1.1em;
        }
        #detailsBox h3 {
            color: #006400;
            margin-top: 0;
            border-bottom: 3px solid #008000;
            padding-bottom: 12px;
            font-size: 1.8em;
            text-align: center;
        }
        /* تأثير وهج خفيف عند التمرير */
    .character::after {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: radial-gradient(circle, rgba(0,255,0,0.15), transparent 70%);
        opacity: 0;
        transition: opacity 0.4s;
    }
    .character:hover::after {
        opacity: 1;
    }
    /* اهتزاز بسيط عند التمرير */
    .character:hover {
        animation: shake 0.3s ease-in-out;
    }
    @keyframes shake {
        0% { transform: translateY(-6px) scale(1.06) translateX(0); }
        25% { transform: translateY(-6px) scale(1.06) translateX(2px); }
        50% { transform: translateY(-6px) scale(1.06) translateX(-2px); }
        75% { transform: translateY(-6px) scale(1.06) translateX(1px); }
        100% { transform: translateY(-6px) scale(1.06) translateX(0); }
    }

    /* إضاءة على الإطار عند التمرير */
    .character:hover {
        border: 2px solid #00cc00 !important;
        box-shadow: 0 0 15px rgba(0,255,0,0.5);
    }

    /* حركة دخول البطاقة عند تحميل الصفحة */
    .character {
        opacity: 0;
        transform: translateY(20px);
        animation: fadeInUp 0.8s ease forwards;
    }
    @keyframes fadeInUp {
        0% { opacity: 0; transform: translateY(20px); }
        100% { opacity: 1; transform: translateY(0); }
    }

    /* تأخير بسيط بين البطاقات */
    .character:nth-child(1) { animation-delay: 0.05s; }
    .character:nth-child(2) { animation-delay: 0.10s; }
    .character:nth-child(3) { animation-delay: 0.15s; }
    .character:nth-child(4) { animation-delay: 0.20s; }
    .character:nth-child(5) { animation-delay: 0.25s; }
    .character:nth-child(6) { animation-delay: 0.30s; }
    .character:nth-child(7) { animation-delay: 0.35s; }
    .character:nth-child(8) { animation-delay: 0.40s; }
    .character:nth-child(9) { animation-delay: 0.45s; }
    .character:nth-child(10) { animation-delay: 0.50s; }
    .character:nth-child(11) { animation-delay: 0.55s; }
    .character:nth-child(12) { animation-delay: 0.60s; }

    /* تأثير ظهور تدريجي للنص داخل مربع التفاصيل */
    #detailsBox {
        animation: fadeText 0.7s ease;
    }
    @keyframes fadeText {
        from { opacity: 0; }
        to { opacity: 1; }
    }
    @keyframes softMove {
        0% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
        100% { background-position: 0% 50%; }
    }
</style>
</head>
<body>

    <h1>الصحابة العمانيون رضي الله عنهم</h1>

    <div class="logos">
        <img src="شعار المكتب.png" alt="شعار المكتب">
        <img src="شعار قسم التعريف بهلا.png" alt="شعار قسم التعريف بهلا">
    </div>

    <h2>اضغط على أي شخصية لعرض معلوماتها التفصيلية</h2>

    <div class="characters-wrapper">
        <div class="character-column" id="column1"></div>
        <div class="character-column" id="column2"></div>
    </div>

    <div id="detailsBox"></div>

<script>
const sahaba = [
 {name: "أَسَد بن يَبْرَحَ", info: "هو **أَسَد بن يَبْرَحَ الطاحي**. أسلم ضمن وفد عُمان الذي قدم إلى النبي ﷺ، وسأله أن يبعث معهم رجلًا ليُعلّمهم شرائع الإسلام، مما يدل على مكانته ورجاحة عقله. يُرجح كونه رئيسًا على الوفد الذي قدم إلى الرسول ﷺ مسلماً. صحابته موثقة عند ابن سعد والنويري وغيرهم."},
 {name: "الخِرِّيت بن راشد", info: "هو **الخِرِّيت بن راشد النّاجي العَبْدي السّامي القرشي**. التقى النبي ﷺ في وفد بني سامة بن لؤي بين مكة والمدينة، حيث أكرمهم النبي. كان رئيسًا لقومه، وتولى مناصب قيادية؛ حيث كان واليًا على كور فارس في عهد عثمان، وواليًا على الأهواز في عهد علي بن أبي طالب. أكد ابن الأثير وابن حجر كونه صحابياً وعمانياً."},
 {name: "ذَهْبَن بن قِرْضِم", info: "هو الصحابي الجليل **ذَهْبَن بن قِرْضِم المهري**. وفد على النبي ﷺ بمفرده من ديار مهرة (جنوب عُمان - الشحر). أكرمه النبي ﷺ وقربه، وزوده ببتّته، وكتب له كتاباً، مما يدل على مكانته. ذكر في كتب تراجم الصحابة."},
 {name: "سَلَمَة بن عياذ", info: "هو **سَلَمَة بن عِياذ الأزدي**. جاء مع وفد من الأزد وسأل النبي ﷺ عن دعوته قبل إسلامه، ثم أعلن إسلامه ودعا لقومه أن يجمع الله كلمتهم. تميز برجاحة العقل وله رواية في الحديث."},
 {name: "صالح بن المتوكل", info: "أبو كثير **صالح بن المتوكل الطائي**، مولى الصحابي مازن بن غضوبة. أسلم معه، وهو ثاني من أسلم من أهل عُمان. سأله النبي ﷺ وقال لمازن: (استوصِ به خيرًا). استشهد في برذعة بأذربيجان عام 25هـ."},
 {name: "عبد الله بن عَلَس", info: "هو **عبد الله بن عَلَس الثمالي**. قدم مع مُسْلية بن هِزّان بعد فتح مكة، وبايعوا النبي ﷺ وكتب لهم كتاباً يحدد ما فرض عليهم من الصدقة. كان زعيماً في قومه ومشهوراً بالسبق إلى الإسلام."},
 {name: "كَعْب بن بَرْشَة", info: "هو **كعب بن برشة العودي الطاحي**. كان قارئاً للكتب النصرانية، وأرسله عامل كسرى للتحقق من دعوة النبي ﷺ. أسلم بعد أن عرف صفات النبوة التي قرأها. يعد من أوائل من أسلم من أهل عُمان."},
 {name: "مازن بن غضوبة", info: "هو **مازن بن غضوبة الطائي**، أول من أسلم من أهل عُمان. سمع صوتاً من صنمه يخبره بظهور النبي ﷺ، فذهب إلى المدينة وأعلن إسلامه. دعا له النبي ﷺ بالولد فرُزق بابنه حَيّان. يُرجح استشهاده في أذربيجان."},
 {name: "مُسْلِيَة بن هِزَّان", info: "هو **مُسْلية بن هِزّان الحُدّاني**. أسلم بعد فتح مكة ومعه رهط من قومه، وكتب لهم النبي ﷺ كتاباً. كان زعيماً لقومه، وله أثر كبير في الدعوة في مناطق صحار وما حولها."},
 {name: "مِنْجاب بن راشد", info: "الصحابي الجليل **منجاب بن راشد الناجي**، أخو الخريت بن راشد. التقى النبي ﷺ في الطريق مع وفد بني سامة. ذُكر ممن تولوا مناصب في فارس في عهد عثمان."},
 {name: "مَهْري بن الأبيض", info: "هو **مهري بن الأبيض المهري**. قدم بوفد قبيلة مهرة، فأسلموا وكتب لهم النبي ﷺ كتاباً ينظم شؤونهم. كان له دور كبير في دعم الدعوة الإسلامية في الجنوب العماني."},
 {name: "عَكْنَاء بنت أبي صُفْرَة", info: "هي الصحابية **عكناء بنت أبي صفرة الأزدية**. ذكرها ابن الأثير وابن حجر وغيرهما. عمانية النسب، ويحتمل إسلامها مع أبيها وإخوتها."}
];

const column1 = document.getElementById('column1');
const column2 = document.getElementById('column2');
const detailsBox = document.getElementById('detailsBox');

function renderCharacters() {
 column1.innerHTML = '';
 column2.innerHTML = '';
 sahaba.forEach((p, i) => {
   const c = document.createElement('div');
   c.className = 'character';
   c.textContent = p.name;
   c.onclick = () => showDetails(i);
   if (i < 6) column1.appendChild(c); else column2.appendChild(c);
 });
}

function showDetails(i) {
 const p = sahaba[i];
 detailsBox.innerHTML = `<h3>${p.name} رضي الله عنه/عنها</h3><p>${p.info}</p>`;
 detailsBox.style.display = 'block';
 detailsBox.scrollIntoView({ behavior: 'smooth' });
}

window.onload = renderCharacters;
</script>

</body>
</html>
