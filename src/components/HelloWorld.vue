<template>
  <div class="hello">
    <div class="container">
      <div class="row">
        <div class="col-3"></div>
        <div class="col-6">
          <h1>{{ msg }}</h1>
          <div id="textbox" style="margin-top: 5rem">
            <h4 style="text-align: justify">{{ quotes[numberrr].quotetext }}</h4>
            <h5 style="text-align: justify">-<br>{{ quotes[numberrr].translation }}</h5>
            <h5> - {{ quotes[numberrr].author }}</h5>
            <button type="button" class="btn btn-primary" v-on:click="numberrr = randomElement()">Get Quote!</button>
          </div>
        </div>
        <div class="col-3"></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
      //randomNumber: randomElement()
    },
    data() {
      return {
        quotes: [{
            id: 1,
            title: "",
            quotetext: "“A room without books is like a body without a soul”",
            author: "Marcus Tullius Cicero",
            translation: ""
          },
          {
            id: 2,
            title: "",
            quotetext: "“Наука борется с суевериями, как свет с потемками”",
            author: "Dmitri Ivanovich Mendeleev",
            translation: "Science fights superstition like light against darkness"
          },
          {
            id: 3,
            title: "",
            quotetext: "“If you have a garden and a library, you have everything you need”",
            author: "Marcus Tullius Cicero",
            translation: ""
          },
          {
            id: 4,
            title: "",
            quotetext: "“Everyone sees what you appear to be, few experience what you really are.”",
            author: "Niccolò Machiavelli, The Prince",
            translation: ""
          },
          {
            id: 5,
            title: "",
            quotetext: "“В человеке должно быть всё прекрасно: и лицо, и одежда, и душа, и мысли”",
            author: "Anton Pavlovich Chekhov",
            translation: "Everything in a person should be beautiful: face, clothes, soul, and thoughts"
          },
          {
            id: 6,
            title: "",
            quotetext: "“Дело не в пессимизме и не в оптимизме, а в том, что у девяноста девяти из ста нет ума”",
            author: "Anton Pavlovich Chekhov",
            translation: "It’s not pessimism or optimism, but that ninety-nine out of a hundred have no mind"
          },
          {
            id: 7,
            title: "",
            quotetext: "“Wonder is the desire of knowledge”",
            author: "St. Thomas Aquinas",
            translation: ""
          },
          {
            id: 8,
            title: "",
            quotetext: "“By prevailing over all obstacles and distractions, one may unfailingly arrive at his chosen goal or destination”",
            author: "Christopher Columbus",
            translation: ""
          },
          {
            id: 9,
            title: "",
            quotetext: "“Перестать читать книги — значит перестать мыслить”",
            author: "Fyodor Mikhailovich Dostoyevsky",
            translation: "To stop reading books is to stop thinking"
          },
          {
            id: 10,
            title: "",
            quotetext: "“Вся гордость учителя в учениках, в росте посеянных им семян”",
            author: "Dmitri Ivanovich Mendeleev",
            translation: "All the pride of the teacher is in the students, in the growth of the seeds sown by him"
          },
          {
            id: 11,
            title: "",
            quotetext: "“Every particle of matter is attracted by or gravitates to every other particle of matter with a force inversely proportional to the squares of their distances”",
            author: "Isaac Newton",
            translation: ""
          },
          {
            id: 12,
            title: "",
            quotetext: "“Excellence is never an accident. It is always the result of high intention, sincere effort, and intelligent execution; it represents the wise choice of many alternatives - choice, not chance, determines your destiny”",
            author: "Aristotle",
            translation: ""
          },
          {
            id: 13,
            title: "",
            quotetext: "“Кто жил и мыслил, тот не может в душе не презирать людей”",
            author: "Alexander Sergeyevich Pushkin",
            translation: "Who lived and thought, he cannot help but despise people in his soul"
          },
          {
            id: 14,
            title: "",
            quotetext: "“To one who has faith, no explanation is necessary. To one without faith, no explanation is possible”",
            author: "St. Thomas Aquinas",
            translation: ""
          },
          {
            id: 15,
            title: "",
            quotetext: "“Надо любить жизнь больше, чем смысл жизни”",
            author: "Fyodor Mikhailovich Dostoyevsky",
            translation: "One must love life more than the meaning of life"
          },
          {
            id: 16,
            title: "",
            quotetext: "“We must love them both, those whose opinions we share and those whose opinions we reject, for both have labored in the search for truth, and both have helped us in finding it”",
            author: "St. Thomas Aquinas",
            translation: ""
          },
          {
            id: 17,
            title: "",
            quotetext: "“If an injury has to be done to a man it should be so severe that his vengeance need not be feared”",
            author: "Niccolo Machiavelli, The Prince",
            translation: ""
          },
          {
            id: 18,
            title: "",
            quotetext: "“He made an instrument to know/If the moon shine at full or no”",
            author: "Aristotle",
            translation: ""
          },
          {
            id: 19,
            title: "",
            quotetext: "“If I had my life to live over again, I would have made a rule to read some poetry and listen to some music at least once every week”",
            author: "Charles Darwin",
            translation: ""
          },
          {
            id: 20,
            title: "",
            quotetext: "“Beware the man of a single book”",
            author: "St. Thomas Aquinas",
            translation: ""
          },
          {
            id: 21,
            title: "",
            quotetext: "“Жизнь — как езда на велосипеде. Чтобы сохранять равновесие, ты должен двигаться”",
            author: "Albert Einstein",
            translation: "Life is like riding a bicycle. To keep your balance you must move"
          },
          {
            id: 22,
            title: "",
            quotetext: "“Don’t walk in front of me… I may not follow Don’t walk behind me… I may not lead Walk beside me… just be my friend”",
            author: "Albert Camus",
            translation: ""
          },
          {
            id: 23,
            title: "",
            quotetext: "“Я, сколько ни любил бы вас, Привыкнув, разлюблю тотчас”",
            author: "Alexander Sergeyevich Pushkin",
            translation: "No matter how much I love you, accustomed, I will stop loving you immediately"
          },
          {
            id: 24,
            title: "",
            quotetext: "“Моя вера — это вера в то, что счастье человечеству даёт прогресс науки”",
            author: "Ivan Petrovich Pavlov",
            translation: "My belief is the belief that the progress of science gives happiness to humanity"
          },
          {
            id: 25,
            title: "",
            quotetext: "“Помните, что наука требует от человека всей его жизни. И если у вас было бы две жизни, то их не хватило бы вам. Большего напряжения и великой страсти требует наука от человека. Будьте страстны в вашей работе и в ваших исканиях”",
            author: "Ivan Petrovich Pavlov",
            translation: "Remember that science demands from a person his entire life. And if you had two lives, then they would not be enough for you. Science requires more effort and great passion from man. Be passionate about your work and your quest"
          },
          {
            id: 26,
            title: "",
            quotetext: "“I think; therefore I am”",
            author: "Rene Descartes",
            translation: ""
          },
          {
            id: 27,
            title: "",
            quotetext: "“A man who dares to waste one hour of time has not discovered the value of life”",
            author: "Charles Darwin",
            translation: ""
          },
          {
            id: 28,
            title: "",
            quotetext: "“Nobody ever figures out what life is all about, and it doesn't matter. Explore the world. Nearly everything is really interesting if you go into it deeply enough”",
            author: "Richard P. Feynman",
            translation: ""
          },
          {
            id: 29,
            title: "",
            quotetext: "“Стремись не к тому, чтобы добиться успеха, а к тому, чтобы твоя жизнь имела смысл”",
            author: "Albert Einstein",
            translation: "Strive not to achieve success, but to ensure that your life has meaning"
          },
          {
            id: 30,
            title: "",
            quotetext: "“Man is the only creature who refuses to be what he is”",
            author: "Albert Camus",
            translation: ""
          },
          {
            id: 31,
            title: "",
            quotetext: "“You have no responsibility to live up to what other people think you ought to accomplish. I have no responsibility to be like they expect me to be. It's their mistake, not my failing”",
            author: "Richard P. Feynman",
            translation: ""
          },
          {
            id: 32,
            title: "",
            quotetext: "“The reading of all good books is like conversation with the finest men of past centuries”",
            author: "Rene Descartes",
            translation: ""
          },
          {
            id: 33,
            title: "",
            quotetext: "“If you would be a real seeker after truth, it is necessary that at least once in your life you doubt, as far as possible, all things”",
            author: "Rene Descartes",
            translation: ""
          },
          {
            id: 34,
            title: "",
            quotetext: "“I suppose therefore that all things I see are illusions; I believe that nothing has ever existed of everything my lying memory tells me. I think I have no senses. I believe that body, shape, extension, motion, location are functions. What is there then that can be taken as true? Perhaps only this one thing, that nothing at all is certain”",
            author: "Rene Descartes",
            translation: ""
          },
          {
            id: 35,
            title: "",
            quotetext: "“Conquer yourself rather than the world”",
            author: "Rene Descartes",
            translation: ""
          },
          {
            id: 36,
            title: "",
            quotetext: "“Every government degenerates when trusted to the rulers of the people alone. The people themselves are its only safe depositories”",
            author: "Thomas Jefferson",
            translation: ""
          },
          {
            id: 37,
            title: "",
            quotetext: "“Educating the mind without educating the heart is no education at all”",
            author: "Aristotle",
            translation: ""
          },
          {
            id: 38,
            title: "",
            quotetext: "“Это просто безумство: делать то же самое и ждать других результатов”",
            author: "Albert Einstein",
            translation: "It's crazy to do the same and wait for different results."
          },
          {
            id: 39,
            title: "",
            quotetext: "“He who is to be a good ruler must have first been ruled”",
            author: "Aristotle",
            translation: ""
          },
          {
            id: 40,
            title: "",
            quotetext: "“井の中の蛙、大海を知らず – I no naka no kawazu, taikai wo sirazu”",
            author: "Japanese wisdom",
            translation: "A frog in a well never knows the vast ocean"
          },
          {
            id: 41,
            title: "",
            quotetext: "“口は災いの元 – Kuchi wa wazawai no moto”",
            author: "Japanese wisdom",
            translation: "A mouth causes trouble"
          },
          {
            id: 42,
            title: "",
            quotetext: "“不作不死。”",
            author: "Chinese wisdom",
            translation: "If you don't do stupid things you won't end up in tragedy"
          },
          {
            id: 43,
            title: "",
            quotetext: "“塞翁失马，焉知非福。”",
            author: "Chinese wisdom",
            translation: "Blessings come in disguise"
          },
          {
            id: 44,
            title: "",
            quotetext: "“小洞不补，大洞吃苦。”",
            author: "Chinese wisdom",
            translation: "If small holes aren't fixed, then big holes will bring hardship"
          },
          {
            id: 45,
            title: "",
            quotetext: "“水满则溢。”",
            author: "Chinese wisdom",
            translation: "Water flows in only to flow out"
          },
          {
            id: 46,
            title: "",
            quotetext: "“读万卷书不如行万里路。”",
            author: "Chinese wisdom",
            translation: "It's better to walk thousands of miles than to read thousands of books"
          },
          {
            id: 47,
            title: "",
            quotetext: "“ 三个和尚没水喝。”",
            author: "Chinese wisdom",
            translation: "Too many cooks spoil the broth"
          },
          {
            id: 48,
            title: "",
            quotetext: "“笑解千愁。”",
            author: "Chinese wisdom",
            translation: "A smile dispels many worries"
          },
          {
            id: 49,
            title: "",
            quotetext: "“美名胜过美貌。”",
            author: "Chinese wisdom",
            translation: "A good name is better than a good face"
          },
          {
            id: 50,
            title: "",
            quotetext: "“不善始者不善终。”",
            author: "Chinese wisdom",
            translation: "A bad beginning makes a bad ending"
          },
          {
            id: 51,
            title: "",
            quotetext: "“大处着眼，小处着手。”",
            author: "Chinese wisdom",
            translation: "Keep the general goal in sight while tackling daily tasks"
          },
          {
            id: 52,
            title: "",
            quotetext: "“In this sign thou shalt conquer”",
            author: "Constantine the Great",
            translation: ""
          },
          {
            id: 53,
            title: "",
            quotetext: "“自業自得”",
            author: "Japanese wisdom",
            translation: "One’s act, one’s profit"
          },
          {
            id: 54,
            title: "",
            quotetext: "“十人十色”",
            author: "Japanese wisdom",
            translation: "Ten men, ten colors"
          },
          {
            id: 55,
            title: "",
            quotetext: "“起死回生”",
            author: "Japanese wisdom",
            translation: "Wake from death and return to life"
          },
          {
            id: 56,
            title: "",
            quotetext: "“我田引水”",
            author: "Japanese wisdom",
            translation: "Pulling water to my own rice paddy"
          },
          {
            id: 57,
            title: "",
            quotetext: "“640K is more memory than anyone will ever need on a computer”",
            author: "Bill Gates",
            translation: ""
          },
          {
            id: 58,
            title: "",
            quotetext: "“悪因悪果”",
            author: "Japanese wisdom",
            translation: "Evil cause, evil effect"
          },
          {
            id: 59,
            title: "",
            quotetext: "“見ぬが花”",
            author: "Japanese wisdom",
            translation: "Not seeing is a flower"
          },
          {
            id: 60,
            title: "",
            quotetext: "“А дело бывало -- и коза волка съедала”",
            author: "Russian wisdom",
            translation: "Pigs might fly. Literal: It was happening -- a goat was eating up a wolf."
          },
          {
            id: 61,
            title: "",
            quotetext: "“Аво́сь да как-нибу́дь до добра́ не доведу́т”",
            author: "Russian wisdom",
            translation: "Draw not your bow till your arrow is fixed. Literal: Maybe and somehow won't make any good"
          },
          {
            id: 62,
            title: "",
            quotetext: "“Азбука -- к мудрости ступенька”",
            author: "Russian wisdom",
            translation: "You have to learn to walk before you can run. Literal: Alphabet is the step to wisdom"
          },
          {
            id: 63,
            title: "",
            quotetext: "“Алты́нного во́ра ве́шают, а полти́нного че́ствуют”",
            author: "Russian wisdom",
            translation: "Little thieves are hanged, but great ones escape. Literal: The thief who stole an altyn (3 kopecks) is hung, and the one who stole a poltinnik (50 kopecks) is praised."
          },
          {
            id: 64,
            title: "",
            quotetext: "“Аппети́т прихо́дит во вре́мя еды́”",
            author: "Russian wisdom",
            translation: "Appetite comes with eating. Literal: The appetite comes during eating"
          },
          {
            id: 65,
            title: "",
            quotetext: "“Арте́льный горшо́к гу́ще кипи́т”",
            author: "Russian wisdom",
            translation: "With a helper a thousand things are possible. Literal: An artel's pot boils denser"
          },
          {
            id: 66,
            title: "",
            quotetext: "“Ахал бы дядя, на себя глядя”",
            author: "Russian wisdom",
            translation: "The devil rebuking sin. Literal: The uncle would better gasp looking at himself."
          },
          {
            id: 67,
            title: "",
            quotetext: "“Ба́ба с во́зу -- кобы́ле ле́гче”",
            author: "Russian wisdom",
            translation: "No women, no cry! Literal: It is easier for the mare when a woman gets off the cart"
          },
          {
            id: 68,
            title: "",
            quotetext: "“Ба́бушка гада́ла, на́двое сказа́ла”",
            author: "Russian wisdom",
            translation: "No one can know for certain. Literal: Granny was telling fortunes, said two things"
          },
          {
            id: 69,
            title: "",
            quotetext: "“Ба́бушка на́двое сказа́ла”",
            author: "Russian wisdom",
            translation: "No one can know for certain. Literal: Granny said two things"
          },
          {
            id: 70,
            title: "",
            quotetext: "“Ба́ры деру́тся -- у холо́пов чубы́ треща́т”",
            author: "Russian wisdom",
            translation: "When the rich make war it's the poor that die. Literal: Masters are fighting, servants' forelocks are creaking"
          },
          {
            id: 71,
            title: "",
            quotetext: "“Без кота́ мыша́м раздо́лье”",
            author: "Russian wisdom",
            translation: "	When the cat is away, the mice will play. Literal: Without a cat mice feel free"
          },
          {
            id: 72,
            title: "",
            quotetext: "“Бережливость хороша, да скупость страшна”",
            author: "Russian wisdom",
            translation: "Economy is a good servant but a bad master"
          },
          {
            id: 73,
            title: "",
            quotetext: "“Бог не вы́даст, свинья́ не съест”",
            author: "Russian wisdom",
            translation: "Literal: God won't give it away, pigs won't eat it"
          },
          {
            id: 74,
            title: "",
            quotetext: "“В глаза льстит, а за глаза пакостит”",
            author: "Russian wisdom",
            translation: "To carry fire in one hand and water in the other"
          },
          {
            id: 75,
            title: "",
            quotetext: "“В гостя́х хорошо́, а до́ма лу́чше”",
            author: "Russian wisdom",
            translation: "There's no place like home.; East or West, home is best. Literal: It is good to be visiting, but it is better at home"
          },
          {
            id: 76,
            title: "",
            quotetext: "“Где говорят деньги, там молчит совесть”",
            author: "Russian wisdom",
            translation: "The money will heal all the hurts of honor. Literal: Where money speak, there the conscience is silent"
          },
          {
            id: 77,
            title: "",
            quotetext: "“На безры́бье и рак -- ры́ба”",
            author: "Russian wisdom",
            translation: "Something is better than nothing. Literal: On a fishing lull, even a crayfish is fish"
          },
          {
            id: 78,
            title: "",
            quotetext: "“На Бо́га наде́йся, а сам не плоша́й”",
            author: "Russian wisdom",
            translation: "Trust in God, but lock your car. Literal: Hope for God, but do not be reliant"
          },
          {
            id: 79,
            title: "",
            quotetext: "“トキヲトマレ”",
            author: "Dio Brando",
            translation: "THE WORLD! TIME STOP YOUR FLOW!"
          },
          {
            id: 80,
            title: "",
            quotetext: "“И в самых благородных семьях бывают скандалы”",
            author: "Russian wisdom",
            translation: "Accidents will happen in the best regulated families. Literal: There are scandals even in the most noble families"
          },
          {
            id: 81,
            title: "",
            quotetext: "“И волки сыты, и овцы целы”",
            author: "Russian wisdom",
            translation: "Have one's cake and eat it too. Literal: The wolves are sated, and the sheep are intact"
          },
          {
            id: 82,
            title: "",
            quotetext: "“На весь свет не угодишь”",
            author: "Russian wisdom",
            translation: "If you try to please all you will please none"
          },
          {
            id: 83,
            title: "",
            quotetext: "“Где любовь и совет, там и горя нет”",
            author: "Russian wisdom",
            translation: "Literal: Where love and advice exists, there is no grief"
          },
          {
            id: 84,
            title: "",
            quotetext: "“Qui sème le vent, récolte la tempête”",
            author: "French wisdom",
            translation: "He who sows the wind shall reap the tempest. (As you sow, so you shall reap.)"
          },
          {
            id: 85,
            title: "",
            quotetext: "“C’est l’exception qui confirme la règle”",
            author: "French wisdom",
            translation: "It’s the exception that proves the rule"
          },
          {
            id: 86,
            title: "",
            quotetext: "“La raison du plus fort est toujours la meilleure. (Jean de La Fontaine – Fables)”",
            author: "French wisdom",
            translation: "The motive of the strongest is always the best. (Might is always right.)"
          },
          {
            id: 87,
            title: "",
            quotetext: "“Il faut manger pour vivre, et non pas vivre pour manger. (Molière – L’Avare)”",
            author: "French wisdom",
            translation: "One must eat to live, and not live to eat"
          },
          {
            id: 88,
            title: "",
            quotetext: "“Revenons à nos moutons”",
            author: "French wisdom",
            translation: "Let us get back to our sheep. (Let’s get back to what we were saying/ doing.)"
          },
          {
            id: 89,
            title: "",
            quotetext: "“Mieux vaut prévenir que guérir”",
            author: "French wisdom",
            translation: "Better to prevent than to cure. (An ounce of prevention is worth a pound of cure.)"
          },
          {
            id: 90,
            title: "",
            quotetext: "“Okuz altinda buzagi aranmaz”",
            author: "Turkish wisdom",
            translation: "(The dog that barks does not bite.) When a person talks too much, it usually does not lead to action"
          },
          {
            id: 91,
            title: "",
            quotetext: "“Havlayan kopek isirmaz”",
            author: "Turkish wisdom",
            translation: "(The cock that crows too early gets his head cut off.) There is proper time for every thing"
          },
          {
            id: 92,
            title: "",
            quotetext: "“Vakitsiz oten horozun basini keserler”",
            author: "Turkish wisdom",
            translation: "(A defeated wrestler never tires of wrestling again.) . A defeated person always asks for second chances"
          },
          {
            id: 93,
            title: "",
            quotetext: "“Yenilen pehlivan gurese doymaz”",
            author: "Turkish wisdom",
            translation: "(He who starts up in anger, sits down with a loss.) Used when one is trying to calm an angry person"
          },
          {
            id: 94,
            title: "",
            quotetext: "“Ofke ile kalkan zararla oturur”",
            author: "Turkish wisdom",
            translation: "(Sharp vinegar only damages its container.) Used to calm down or moderate a person"
          },
          {
            id: 95,
            title: "",
            quotetext: "“El mundo es un pañuelo”",
            author: "Spanish wisdom",
            translation: "The world is a handkerchief"
          },
          {
            id: 96,
            title: "",
            quotetext: "“Thinking is the great enemy of perfection. The habit of profound reflection, I am compelled to say, is the most pernicious of all the habits formed by civilized man.”",
            author: "Constantine the Great",
            translation: ""
          },
          {
            id: 97,
            title: "",
            quotetext: "“A lo hecho, pecho”",
            author: "Spanish wisdom",
            translation: "To what’s done, chest"
          },
          {
            id: 98,
            title: "",
            quotetext: "“Todos los caminos llevan a Roma”",
            author: "Spanish wisdom",
            translation: "All roads lead to Rome"
          },
          {
            id: 99,
            title: "",
            quotetext: "“القرد في عين أمه غزال”",
            author: "Arabic wisdom",
            translation: "Beauty is in the eye of the beholder"
          },
          {
            id: 100,
            title: "",
            quotetext: "“آخرة المعروف الضرب بالكفوف”",
            author: "Arabic wisdom",
            translation: "No good deed goes unpunished"
          },
        ],
        numberrr: this.randomElement(),
      }
    },
    created: function () {
      this.randomElement()
    },
    methods: {
      randomElement: function () {
        return Math.floor(Math.random() * 100);
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>