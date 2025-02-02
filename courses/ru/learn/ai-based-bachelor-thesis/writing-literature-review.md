---
title: "Написание тезиса: Обзор литературы"
description: Быстрый старт работы над бакалаврским тезисом с помощью инструментов, основанных на искусственном интеллекте
metaOptions: [Learn, Быстрый старт работы над бакалаврским тезисом с помощью инструментов, основанных на искусственном интеллекте]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
Итак, мы приступаем к написанию пожалуй самой скучной части любой около-академической работы — литературный поиск и анализ найденных источников. С первого взгляда, ИИ-помощник должен справится с этой задачей лучше всего. Все что он должен сделать — найти в Интернете релевантные работы, получить их текст в каком-то виде и проанализировать его. Однако, в этой задаче было найдено приличное количество подводных камней, речь о которых пойдет дальше.
</RoboAcademyText>

## Первая попытка

Начнем с более простой задачи — используя уже готовый текст Введения, снабдим его релевантными референсами и цитатами, для подтверждения актуальности утверждений. Первоначальный запрос для ChatGPT и Bing Chat выглядит следующим образом (обязательно с указанием количества источников):

<RoboAcademyDialog>

Add 10 references and quotes for Introduction part to support the statements in the text.
</RoboAcademyDialog>

Оба чат-бота справились с задачей расставить источники по тексту… но абсолютно провалились с собственно поиском источников. Проблема в том, что ИИ-помощники вместо настоящих источников стали откровенно выдумывать несуществующие (но очень похожие на настоящие), добавлять их в текст и даже цитировать выдуманных авторов! 

Пример фейкового источника и фейковой цитаты:

<RoboAcademyDialog>

C. Li et al. "Blockchain-based secure and trustworthy data sharing scheme for smart homes." IEEE Transactions on Industrial Informatics, vol. 16, no. 2, pp. 1236-1245, 2020.

"The deployment of smart home systems has led to concerns over data security and privacy. Blockchain technology has been proposed as a solution to these concerns, as it enables secure and trustworthy data sharing among smart home devices. This paper proposes a blockchain-based secure and trustworthy data sharing scheme for smart homes. The proposed scheme uses blockchain to ensure the integrity and confidentiality of data generated by smart home devices."

</RoboAcademyDialog>

Обратите внимание, как натурально он выглядит: соблюден библиографический формат, приведен реально существующий журнал IEEE. От его использования спасает только проверка в Google Scholar.

<RoboAcademyNote title="Warning" type="warning">
  Всегда перепроверяйте ссылки, цитаты, источники, которые вам предлагает ИИ-помощник.
</RoboAcademyNote>

Это проблема называется [эффект галлюцинации](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)), и на текущий момент она вызывает много споров среди экспертов по искусственному интеллекту. Ситуация усугубляется тем, что галлюцинации могут происходить на уровне, когда их проверка будет слишком затратной (например, ИИ может долго и в подробностях описать какой-нибудь сложный феномен из гидродинамики, который на самом деле не существует), что сведет на нет всю помощь ИИ-сервисов из-за их ненадежности. 

Для сравнения, статистика по несуществующим источникам от разных сервисов:

- ChatGPT: 9 из 10 источников фейковые
- Bing Chat: 7 из 10 источников фейковые
- Auto-GPT: не справился с задачей, так как начал зачем-то разрабатывать парсер сайтов с библиографическими записями.

Заметно, что если у ИИ-сервиса есть доступ к Интернету, он работает лучше, но при этом может например создать прямую ссылку на несуществующий источник. Конечно, общая статистика не впечатляет, но тем не менее продолжим, держа эту проблему в голове.

## Уточняем запросы

После нескольких попыток, лучшей тактикой оказалось просить найти источники, скармливая текст Введения по абзацам. Кроме того, оказалось, что ИИ предпочитает выдавать источники на статьи в блогах, форумах и просто сайтах, вместо научных статей. Поэтому стоит указывать конкретные места (журналы IEEE, Springer, веб-архив arXiv, и т.д.), откуда помощник должен выбрать источники:

<RoboAcademyDialog>

Find 5 scientific sources that prove statements in this text. Use only arXiv, IEEE, Springer articles from 2018 to 2023: "THE_PARAGRAPH"
</RoboAcademyDialog>

Этот запрос выполнялся только для Bing Chat, так как ChatGPT совсем не справился с задачей, из-за отсутствия доступа к Интернету. Результаты оказались куда лучше: Bing Chat иногда выдавал все настоящих 5 источников, и даже мог снабдить их кратким описанием, объяснив какой-именно кусок текста этот источник доказывает. Однако, Bing Chat не справился с созданием bibtex-записи для найденных источников (снова выдав галлюцинации), поэтому для их добавления пришлось вручную воспользоваться Google Scholar.


## Переходим к Литературному обзору

Теперь можно приступать к более сложной задаче — полноценному литературному поиску для второго раздела бакалаврской работы. Сначала последуем плану, и напишем два подраздела на следующие топики:

<RoboAcademyDialog>

&mdash; Overview of smart home technology and its security and privacy issues
<br/>&mdash; Introduction to web3 technology and its potential benefits for smart homes
</RoboAcademyDialog>

Был использован следующий запрос:

<RoboAcademyDialog>

Write a literature review with "THE_TOPIC" in 300 words. Write as if you are writing part of a technical scientific article.
</RoboAcademyDialog>

Последнее уточнение о стиле было добавлено, так как ИИ по умолчанию пишет текст, который больше подходит для публикации в блог. В любом случае, первый полученный результат оказался не слишком впечатляющим — в нем было слишком много лишних деталей, например, почти что реклама умных устройств от Amazon. Тем не менее, его можно было использовать как формирования плана этого подраздела текста, с последующими дополнительными запросами по абзацам. В конечном итоге удалось прийти к следующей структуре:

- Описание smart home technology
- Примеры устройств и их использования
- Существующие проблемы smart home technology
- Примеры решений, направленных на эти проблемы
- Недостатки существующих решений

В целом, полученный текст вполне можно использовать для бакалаврской работы. Аналогичная работа была сделана со вторым топиком о web3 технологиях, а затем каждому подразделу были найдены соответствующие источники, по схеме описанной выше.

## Анализ related works в лоб

Стандартная тактика для анализа — найти 5-10 наиболее актуальных и цитируемых работ по тематике, используя мощные сервисы библиографического поиска (Scopus, Web of Science, Google Scholar). Попробуем сделать это, используя следующий запрос:

<RoboAcademyDialog>

Find five most cited technical scientific articles about developing a smart home systems based of web3 or blockchain or smart contract among IEEE, Springer and arXiv articles from 2020 to 2023
</RoboAcademyDialog>

К сожалению, результаты оказались недостаточно качественными:

- ChatGPT подчеркнул, что не имеет доступа к Интернету, и ограничен информацией до 2021. Все 5 предложенных им источников были несуществующими.
- Bing Chat нашел 3 настоящих источника, вместо 5, но к сожалению 1) только два из них было по теме, 2) они не были наиболее цитируемыми (у одного не было цитат вообще), 3) в некоторых случаях источники были фейковыми (ИИ даже выдумал количество цитирования для них).
- Auto-GPT оказался наиболее точным с точки зрения заданной темы, но не смог выбрать именно наиболее цитируемые статьи, даже после уточнения, что нужно пользоваться Google Scholar для этой задачи.

Увы, специализированный литературный поиск по научным статьям еще не по зубам этим ИИ-сервисам, так что проще и быстрее всего найти топ 5 самых цитируемых статей, воспользовавшись Google Scholar, благо. 

После этого, тем или иным образом, нужно получить полные тексты найденных статей. В обычном варианте нам бы пришлось прочитать лично каждую из них, но мы попробуем запросить summary текста у ИИ-помощников. Мы сразу же столкнемся с проблемами:

1) Статьи как правило доступны в PDF варианте, чаще всего в двухколоночном. У чат-ботов просто нет возможности прочитать PDF-файл, а Auto-GPT на текущий момент не может читать этот формат (но он попытался найти решение этой проблемы сам, хоть и неудачно!)

<RoboAcademyTerminal title="AutoGPT">

**SYSTEM:**  Command read_file returned: Error: 'utf-8' codec can't decode byte 0xe2 in position 10: invalid continuation byte
THOUGHTS:  It looks like I am encountering an encoding issue while trying to open the edgechain PDF file. I can try to extract text from the PDF using the 'tika' library and analyze the contents. I'll use the 'execute_shell' command to install the 'tika' library before using it to extract text from the PDF file.

**REASONING:**  Due to encoding issues trying to read the PDF file, I need a different approach to read the contents of the PDF file in order to analyze and summarize the article.

</RoboAcademyTerminal>

В любом случае, PDF-статьи придется конвертировать в текстовый формат (без изображений и таблиц). Для этого можно воспользоваться такими программами как[PyMuPDF](https://pymupdf.readthedocs.io/en/latest/), [GROBID](https://grobid.readthedocs.io/en/latest/Introduction/), и [PDFMiner](https://pdfminersix.readthedocs.io/en/latest/).

2) Есть куда более серьезная проблема, которая по сути не позволяет использовать эти ИИ-инструменты в лоб для анализа целой статьи. К сожалению, в текущем варианте GPT имеет ограниченную длину контекста, из-за чего Auto-GPT просто отказывается начинать анализ, а чат-боты теряют начало разговора:

<RoboAcademyTerminal title="AutoGPT">

openai.error.InvalidRequestError: This model's maximum context length is 8191 tokens, however you requested 15615 tokens (15615 in your prompt; 0 for the completion). Please reduce your prompt; or completion length.

</RoboAcademyTerminal>

## Анализ related works поэтапно

Поэтому, мы немного схитрим, и прогоним через ИИ статьи постранично, каждый раз запрашивая короткий обзор полученного текста. Затем мы соберем эти обзоры вместе, и получим финальный анализ статьи. Для этого достаточно воспользоваться ChatGPT, для примера, один из результатов:

<RoboAcademyDialog>

<ChatGPT/>

EdgeChain: An Edge-IoT Framework and Prototype Based on Blockchain and Smart Contracts

This article describes EdgeChain, a framework, which addresses scalability and security challenges in the Internet of Things domain by leveraging edge computing, blockchain technology, and smart contracts. Authors highlight the weaknesses of IoT devices and centralized cloud computing and proposes edge computing as a solution. The framework employs a permissioned blockchain and an internal currency system to connect IoT devices with edge cloud resources. Smart contracts enforce regulations and automate policy enforcement.

The paper outlines the key features of the EdgeChain framework, including permissioned blockchain, credit-based resource management, smart contract enforcement, compatibility with legacy devices, and distributed deployment options. It explains the modules of the framework, such as the IoT Proxy, smart contracts interface, blockchain server, and application interface.

Furthermore, the text delves into the deployment of blockchain, development of smart contracts, device registration, and IoT behavior regulation within the EdgeChain framework. It emphasizes thorough testing, legacy device support, and monitoring of device behaviors for policy enforcement.

Overall, the EdgeChain framework shows promise in addressing scalability and security challenges in the IoT domain through the integration of edge computing, blockchain, and smart contracts. The prototype evaluation indicates its potential as a secure and distributed platform for future IoT applications.

</RoboAcademyDialog>

<RoboAcademyText>

Далее остается повторить таким же образом анализ остальных статей, и вуаля, у нас готов полноценный Литературный обзор для нашей бакалаврской работы. В конечном итоге, от нас  потребовалось выбрать лучшие статьи, достать их тексты, и проверить полученные от ИИ-результаты и собрать их в адекватный текст вместе с ссылками на источники. Вся задача заняла около 2 дней, вместо стандартных 2-3 недель.

Теперь мы можем перейти к собственно сути тезиса — непосредственно описанию Методов нашей работы.

</RoboAcademyText>