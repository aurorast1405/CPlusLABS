# CPlusLABS

> Software Engineering C++ course y23/24 by Roriks
> 

→→→ репо предназначен как архив моих лаб, чтобы я не хранила их на ноуте и не захламляла его тем самым. Также  не против, если этим будут пользоваться потомки. Просьба код не копипастить, но смотреть можно, если что-то непонятно — можно даже написать мне в tg (@Rorikss), отвечу по возможности. Буду не против если накидаете звездочки или что-то вроде, мелочь, а приятно.

Тут, опять же, хранятся лишь мое виденье лаб и моя реализация. Исполнение лаб не всегда идеальено и красивое, тут есть что поменять, я вижу это уже сейчас, есть даже ошибочки. В целом, постараюсь оставить тут заметки на отдельные моменты лаб, которые я бы поменяла или которые влекут ошибки и их рил нужно поменять. 

### [lab №3] песочная куча

- следовало бы разнести код на папки, типо lib/bin etc.
- !написать **деструктор** к куче, там memory leak
- в целом у проекта не самая крутая структура. Вроде и ок, а вроде сам sandpile вышел очень обхекмным и перегруженным. Возможно, было бы эстетичней вынести некоторые методы в вспомогательную структурку, дабы почистить код. Некоторые методы оч похожи — лучше вынести в шаблонные или какие-то общие
- А и да, эффективнее рассыпать кучу так: пробежаться по всем клеткам, посмотреть кула расщиряться, расшириться, потом рассыпаться

### [lab №6] песочная куча

- я бы сделала более аестетик хедер.
    - стоит отвести допустим первые 2 байта под размер кодирования, которые будет закодирован хеммингом типо 7/4 всегда стандартным.
    - сейчас имя файла ограничено и всегда одинаково. можно прописать как-то еще размер названия + название
    - в целом весь header можно вынести в отдельную сущность, но это что-то из изменения архитектуры
