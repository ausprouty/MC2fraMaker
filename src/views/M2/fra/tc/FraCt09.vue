<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    localStorage.setItem("lastpage", this.$route.name)
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('fra-tc-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>9.</h1></div>
                        <div class="chapter_title ltr"><h1>Comment prier</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p><em>&laquo;&nbsp;Maman&nbsp;&raquo;, demanda l&rsquo;enfant. &laquo;&nbsp;qu&rsquo;est-ce que la pri&egrave;re?</em><br />
<br />
<em>Maman r&eacute;pondit, &laquo;&nbsp;c&rsquo;est l&rsquo;entretien entre deux personnes qui s&rsquo;aiment&nbsp; &mdash; l&rsquo;une&nbsp; d&rsquo;entre elles est&nbsp; Dieu, et l&rsquo;autre c&rsquo;est toi.&nbsp;&raquo;</em><br />
<br />
La pri&egrave;re, c&rsquo;est communiquer simplement avec le P&egrave;re, qui nous aime sans condition. Le &laquo;&nbsp;num&eacute;ro d&rsquo;urgence&nbsp;&raquo; le bien connu qui relie Washington, D.C. &agrave; Kremlin offre au Pr&eacute;sident une communication instantan&eacute;e et directe avec l&rsquo;Union Sovi&eacute;tique en cas d&rsquo;&eacute;tat d&rsquo;urgence. Si nous comparons cela aux num&eacute;ros de communication entre le croyant et Dieu, la triste v&eacute;rit&eacute; est que notre &laquo;&nbsp;num&eacute;ro d&rsquo;urgence&nbsp;&raquo; spirituel qui touche le c&oelig;ur de Dieu reste au repos la plupart du temps. Nous semblons oublier que le num&eacute;ro existe, jusqu&rsquo;&agrave; ce qu&rsquo;une urgence ou une crise survienne pour nous rappeler que nous ne nous suffisons pas.</p>

<h2>Qui Peut Prier?</h2>

<p>Instinctivement, l&rsquo;homme sait qu&rsquo;il doit prier, et il le faut, m&ecirc;me si c&rsquo;est &agrave; l&rsquo;endroit des dieux faits de bois et de pierre. Toutes les fois que nous&nbsp; sommes confront&eacute;s &agrave; une trag&eacute;die, une&nbsp; peine de c&oelig;ur, un chagrin ou un danger, nous reconnaissons en nous le besoin de nous tourner vers quelqu&rsquo;un plus grand que nous-m&ecirc;me et dont la puissance d&eacute;passe nos circonstances. Mais le danger r&eacute;side dans le fait de prier par ignorance. Apr&egrave;s avoir adress&eacute; leur pri&egrave;re aux dieux de sang, du feu et de la guerre, les hommes paraissent sadiques, impitoyables et militaristes. L&rsquo;homme s&rsquo;int&egrave;gre le caract&egrave;re moral de l&rsquo;objet qu&rsquo;il adore. Cela s&rsquo;applique aussi bien au chr&eacute;tien.<br />
<br />
L&rsquo;Ecriture fait comprendre qu&rsquo;&nbsp;&laquo;&nbsp;il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme&nbsp;&raquo; (1 Timoth&eacute;e 2:5). J&eacute;sus dit, &laquo;&nbsp;Je suis le chemin, la v&eacute;rit&eacute;, et la vie. Nul ne vient au P&egrave;re que par moi (Jean 14:6).&nbsp;&raquo; ceci parait exclusif?&nbsp; C&rsquo;est exactement ce que J&eacute;sus a l&rsquo;intention de dire &mdash;&nbsp; pour nous montrer que le chemin qui m&egrave;ne &agrave; Dieu est tr&egrave;s &eacute;troit, et nous devons nous concentrer sur Lui et non sur quelqu&rsquo;un d&rsquo;autre. Il doit &ecirc;tre notre seul objet d&rsquo;adoration, car &laquo;&nbsp;Nous tous qui, le visage d&eacute;couvert, contemplons comme dans un miroir la gloire du Seigneur, nous sommes transform&eacute;s en la m&ecirc;me image&nbsp;&raquo;<br />
(2 Corinthiens 3:18). Nous adorons le seul vrai Dieu, saint et d&rsquo;amour; et nous focalisant sur Lui&nbsp; fait que nous Lui ressemblons chaque jour.<br />
<br />
La pri&egrave;re requiert un c&oelig;ur pur. Imaginez que nous avons &eacute;t&eacute; invit&eacute;s &agrave; d&icirc;ner avec la Reine d&rsquo;Angleterre. Quelle vague de pr&eacute;paration aurait lieu! Pendant des jours nous ferions des emplettes juste pour la tenue convenable pour l&rsquo;occasion. Nous apparaitrions devant Sa Majest&eacute;, bien pr&eacute;par&eacute;s de la t&ecirc;te aux pieds avec une coupe de cheveux appropri&eacute;e et un discours pr&ecirc;t &agrave; &eacute;viter les erreurs embarrassantes.<br />
<br />
Dieu nous demande seulement d&rsquo;apporter &agrave; Sa pr&eacute;sence un c&oelig;ur pur et ouvert. Le&nbsp; bien-aim&eacute; psalmiste dit, &laquo;&nbsp;Si j&rsquo;avais con&ccedil;u l&rsquo;iniquit&eacute; dans mon c&oelig;ur, Le Seigneur ne m&rsquo;aurait pas exauc&eacute;.&nbsp;&raquo;&nbsp;(Psaumes 66:18). Notre Dieu saint ne peut pas communier avec le p&eacute;ch&eacute;, c&rsquo;est un s&eacute;parateur &eacute;ternel. Si nous voulons que Dieu entende nos pri&egrave;res, nous devons confesser tout p&eacute;ch&eacute; dans nos vies et entrer dans Ses chambres, habill&eacute;s en robes de puret&eacute;.<br />
<br />
Nous osons nous approcher de Son tr&ocirc;ne avec nos requ&ecirc;tes et nos louanges seulement sous l&rsquo;autorit&eacute; de Son Fils le Seigneur J&eacute;sus-Christ. Il est notre seul m&eacute;diateur. A la veille de Sa crucifixion, J&eacute;sus dit pas moins de six fois, &laquo;&nbsp; Si vous demandez quelque chose en mon nom, je le ferai.&nbsp;&raquo; (Voir Jean 14:13-16).</p>

<h2>Qui prions-nous?</h2>

<p>Chaque membre de la trinit&eacute; est impliqu&eacute; dans nos pri&egrave;res. Nous prions le P&egrave;re au nom du Fils &agrave; travers le minist&egrave;re du Saint-Esprit. La pri&egrave;re nous fait entrer dans la pr&eacute;sence du Roi des rois et le Seigneur des seigneurs, et nous-nous inclinons en r&eacute;v&eacute;rence et crainte. Mais Il est notre P&egrave;re et prend plaisir &agrave; notre communication. Pour cela, nous pouvons venir devant Lui confiant et d&eacute;tendu, avec des c&oelig;urs joyeux et remplis d&rsquo;esp&eacute;rance. Dieu nous aime plus que jamais un &ecirc;tre humain ne le pourrait.</p>

<h2>Pourquoi nous prions?</h2>

<ol>
	<li>Nos pri&egrave;res donnent gloire &agrave; Dieu. Bien que notre Seigneur prenne plaisir &agrave; nos louanges et nos requ&ecirc;tes, le but de la pri&egrave;re est de Le glorifier. J&eacute;sus dit, &laquo;&nbsp;et tout ce que vous demanderez en mon nom, je le ferai, afin que le P&egrave;re soit glorifi&eacute; dans le Fils.&nbsp;&raquo; (Jean 14:13).</li>
	<li>Nous communiquons avec Dieu par la pri&egrave;re. Certains prennent la pri&egrave;re pour une &laquo;&nbsp;issue de secours&nbsp;&raquo; convenable pour se tirer d&rsquo;ennui, un chemin direct pour arriver &agrave; leurs fins, et un moyen de manipuler Dieu &agrave; r&eacute;pondre &agrave; leurs besoins. Se servir de la pri&egrave;re de cette fa&ccedil;on c&rsquo;est comme remplir&nbsp; une&nbsp; cadillac (voiture) flambant neuve avec des ballons. La pri&egrave;re est faite pour &ecirc;tre plus que &ccedil;a. La pri&egrave;re est un num&eacute;ro saint de communication, institu&eacute; et ordonn&eacute; par Dieu pour un usage exclusif de Ses pr&eacute;cieux enfants. Le Nouveau Testament est rempli de directives au sujet de la pri&egrave;re et son r&ocirc;le dans la marche chr&eacute;tienne. Paul dit,&nbsp; &laquo;&nbsp;Priez sans cesse&nbsp;&raquo; (1 Thessaloniciens 5:17); &laquo;&nbsp;veillez et priez&nbsp;&raquo; (Matthieu 26:41); &laquo;&nbsp;Priez par l&rsquo;esprit&nbsp;&raquo; (1 Corinthiens 14:15). La pri&egrave;re est importante pour Dieu et vital pour nous. Nous ne pouvons pas grandir sans elle.</li>
	<li>La pri&egrave;re, c&rsquo;est la communion entre Dieu et Ses enfants. Dieu attend avec impatience que nous venions &agrave; Lui dans la pri&egrave;re. Par envie de communion, Il cr&eacute;a l&rsquo;homme. Son amour pour nous &eacute;tait si parfait, si ardent, que malgr&eacute; notre &eacute;gocentrisme, Il a donn&eacute; Son Fils unique pour payer le prix du p&eacute;ch&eacute; et ouvrir un chemin pour que nous venions en Sa pr&eacute;sence. Aussi incroyable que cela puisse paraitre, Dieu veut notre communion&nbsp;! Le livre de Proverbes nous dit &laquo;&nbsp;Mais la pri&egrave;re des hommes droits Lui est&nbsp; agr&eacute;able&nbsp;&raquo; (Proverbes 15:8). Dans nos pens&eacute;es &eacute;go&iuml;stes, la pri&egrave;re est devenue quelque chose pour nous. Quelque chose que nous faisons pour satisfaire nos besoins. Mais on nous dit ici que la pri&egrave;re r&eacute;pond au besoin en Dieu, et que nous devons passer de temps avec Lui, parce que nos pri&egrave;res sont des dons que nous offrons pour plaire et r&eacute;jouir le Seigneur que nous aimons.</li>
	<li>Christ nous a donn&eacute;s un exemple de pri&egrave;re. Quand J&eacute;sus &eacute;tait ici parmi nous, la pri&egrave;re pour Lui &eacute;tait une priorit&eacute;. M&ecirc;me les jours qui sont charg&eacute;s du matin au soir avec un emploi du temps impossible et contraignant,&nbsp; J&eacute;sus trouvait du temps pour la pri&egrave;re. Il &eacute;tait d&eacute;pendant de cette communion avec le P&egrave;re. Il se refugiait dans la pri&egrave;re et restaurait Son esprit froiss&eacute;. Combien plus devrions-nous prendre conscience de notre propre besoin de la pri&egrave;re?</li>
	<li>La pri&egrave;re apporte des r&eacute;sultats. La pri&egrave;re change bien s&ucirc;r les choses. J&eacute;sus a pri&eacute; pour Lazare qui &eacute;tait mort, et Dieu a ramen&eacute; un ami bien aim&eacute; &agrave; la vie (Jean 11:43). Elie a pri&eacute;&nbsp; Dieu pour qu&rsquo;il ne pl&ucirc;t point, et&nbsp; il ne tomba point de pluie sur la terre pendant trois ans et six mois . Lorsqu&rsquo;il pria Dieu de nouveau&nbsp; pour qu&rsquo;Il fasse pleuvoir, le ciel donna de la pluie et la terre produisit son fruit (Jacques 5:17-18). Il y a une puissance ind&eacute;niable dans la pri&egrave;re du croyant.</li>
	<li>La pri&egrave;re est une nourriture spirituelle pour l&rsquo;&acirc;me en croissance. Parler &agrave; Dieu et &eacute;couter Sa r&eacute;ponse fait partir de Son plan pour nous nourrir pendant que nous devenons mature en Lui. Tel qu&rsquo;un petit enfant a besoin de la nourriture et de l&rsquo;amour pour grandir et &ecirc;tre fort physiquement, nous avons besoin de la nourriture d&rsquo;une mani&egrave;re r&eacute;guli&egrave;re pour nos &acirc;mes si nous voulons grandir spirituellement. Parfois, nous pouvons passer une journ&eacute;e et oublier de nous nourrir de la Parole de Dieu ou de communiquer avec le P&egrave;re, sans qu&rsquo;il n&rsquo;y ait aucun effet apparent d&rsquo;inconv&eacute;nient. Mais si nous continuons par nous priver de la nourriture r&eacute;guli&egrave;re, nous allons rapidement commencer par montrer des signes de la malnutrition spirituelle. Pendant les moments de pression, nous nous rendrons compte que nous avons perdu la force de vivre une vie victorieuse et fructueuse.</li>
</ol>

<h2>Quand devons-nous prier?</h2>

<p>On nous demande de prier&nbsp; sans cesse, pour parler de toutes choses &agrave; Dieu, pour tirer&nbsp; des &laquo;&nbsp;fl&egrave;ches de pri&egrave;re&nbsp;&raquo; dans Sa direction pendant que nous traversons la journ&eacute;e. Nous demandons de la sagesse&nbsp; pendant les difficult&eacute;s. Nous Le remercions pour les b&eacute;n&eacute;dictions pendant qu&rsquo;elles arrivent. Nous prions pour le salut des bien-aim&eacute;s, et pour la gu&eacute;rison des maladies. Nous prions pour la sagesse de nos leaders, pour nos pasteurs et les politiciens. Et tout ceci se fait pendant que la vie suit son cours autour de nous, sur l&rsquo;autoroute, dans la cuisine avec des enfants suspendus au genoux, et en marchant dans notre bureau.<br />
<br />
Mais il y a aussi un besoin de disposer de temps seul dans un endroit isol&eacute; o&ugrave; nous pouvons tranquillement nous mettre &agrave; genou devant Dieu avec une Bible ouverte et parler paisiblement avec Lui pendant que nous lisons Sa Parole. Nous entendons la voix de Dieu &agrave; travers Sa Parole et&nbsp; &agrave; travers les impressions qui nous viennent pendant que nous ouvrons nos c&oelig;urs pour m&eacute;diter en Sa pr&eacute;sence.<br />
<br />
Pendant que vous lisez la Bible, demandez au Saint-Esprit de rendre votre lecture significative et &eacute;difiante. Faites souvent une pause pour remercier Dieu pour Ses provisions empreintes d&rsquo;amour, pour confesser les faiblesses qui se trouvent dans votre vie tel que l&rsquo;Ecriture les r&eacute;v&egrave;le, pour demander l&rsquo;audace et la foi qu&rsquo;avaient les ap&ocirc;tres, et Le remercier, pour une nouvelle id&eacute;e de Son plan pour votre vie. Inviter Dieu &agrave; vous parler, puis attendez pour &eacute;couter Sa voix.<br />
<br />
La pri&egrave;re en groupe dans l&rsquo;entreprise d&rsquo;autres chr&eacute;tiens constitue une part vitale pour une vie de pri&egrave;re active. Toutefois, quelques rassemblements sont plus monotones, non attractifs et ennuyeux qu&rsquo;une rencontre ordinaire de pri&egrave;re. C&rsquo;est le manque de pr&eacute;paration individuelle qui cr&eacute;e le vide que nous sentons dans&nbsp;&nbsp; de pareils moments. Lorsque nous passons de temps avec Dieu en priv&eacute;, se pr&eacute;parant pour le temps que nous allons passer ensemble, nous venons d&eacute;j&agrave; rempli de Sa pr&eacute;sence, esp&eacute;rant qu&rsquo;Il fasse de grandes choses pendant que nous sommes en Sa pr&eacute;sence.&nbsp; Sans la pr&eacute;paration, nous ne pouvons que prendre les pri&egrave;res de quelqu&rsquo;un d&rsquo;autre que nous fa&ccedil;onnons, et notre c&oelig;ur n&rsquo;est pas dans ce&nbsp; que nous disons.<br />
<br />
Combien il est excitant de parler &agrave; Dieu avec la pens&eacute;e qu&rsquo;Il est vraiment pr&eacute;sent &mdash; pendant qu&rsquo;Il l&rsquo;est vraiment. Les pri&egrave;res sont sinc&egrave;res et spontan&eacute;es, dirig&eacute;es par le Saint-Esprit.<br />
Qu&rsquo;est-ce qui est inclus dans la pri&egrave;re?<br />
<br />
Nous pouvons facilement nous rappeler les &eacute;l&eacute;ments fondamentaux de la pri&egrave;re en utilisant le mot &ldquo;ACRS&rdquo; pour m&eacute;moire: adoration, confession, reconnaissance et supplication.<br />
<br />
<strong>Adoration. </strong>Adorer Dieu c&rsquo;est Le v&eacute;n&eacute;rer et Le louer, L&rsquo;honorer et L&rsquo;exalter dans nos c&oelig;urs et nos pens&eacute;es. Nos pri&egrave;res doivent &ecirc;tre une expression d&rsquo;une confiance compl&egrave;te en Lui, l&rsquo;assurance qu&rsquo;Il nous &eacute;coute. La pri&egrave;re est plus que des mots. C&rsquo;est l&rsquo;expression de nos c&oelig;urs qui sont ouverts devant Dieu.<br />
<br />
Lire les cantiques de louange &agrave; haut voix, et des portions similaires de l&rsquo;Ecriture peut grandement enrichir nos moments de pri&egrave;re. Le temps pass&eacute; en louant Dieu pour Sa bont&eacute; va r&eacute;chauffer le c&oelig;ur le plus froid.<br />
<br />
<strong>Confession.</strong> Pour le chr&eacute;tien qui recherche la communion avec Dieu,&nbsp; il faut commencer la pri&egrave;re par la confession sur la base de Psaumes 66:18: &laquo;&nbsp;Si j&rsquo;avais con&ccedil;u l&rsquo;iniquit&eacute; dans mon c&oelig;ur, Le Seigneur ne m&rsquo;aurait pas exauc&eacute;.&nbsp;&raquo; Esa&iuml;e 59:2 nous rappelle, &laquo;&nbsp;Mais ce sont vos crimes qui mettent une s&eacute;paration Entre vous et votre Dieu&nbsp;; Ce sont vos p&eacute;ch&eacute;s qui vous cachent sa face Et l&rsquo;emp&ecirc;chent de vous &eacute;couter.&nbsp;&raquo;&nbsp; Confesser notre p&eacute;ch&eacute; pr&eacute;pare le c&oelig;ur &agrave; l&rsquo;action de gr&acirc;ce et la supplication.<br />
<br />
Si notre discipline de pri&egrave;re commence avec une adoration de r&eacute;v&eacute;rence adress&eacute;e &agrave; Dieu, tout p&eacute;ch&eacute; qui se trouve dans nos vie sera r&eacute;v&eacute;l&eacute; par le Saint-Esprit. Car, en voyant Dieu dans Sa saintet&eacute; et Son amour, nous prenons conscience de notre propre p&eacute;ch&eacute; et de notre indignit&eacute;. Quelqu&rsquo;un habill&eacute; en blanc qui entre dans une mine de charbon sombre ne saura pas combien il est devenu tach&eacute; et sale jusqu&rsquo;&agrave; ce qu&rsquo;il apparaisse de nouveau &agrave; la lumi&egrave;re. C&rsquo;est la m&ecirc;me chose avec le p&eacute;ch&eacute;. Jusqu&rsquo;&agrave; ce que nous nous exposions &agrave; la &laquo;&nbsp;lumi&egrave;re du monde&nbsp;&raquo; (J&eacute;sus), nous ne pouvons pas voir les endroits sombres dans nos vies.<br />
<br />
Nous pouvons toujours &ecirc;tre totalement ouverts avec Dieu, car Il nous connait intimement. Nous n&rsquo;avons aucun secret devant Lui. Les cheveux de notre t&ecirc;te sont compt&eacute;s, et Il connait nos pens&eacute;es avant que nous ne les concevions. Nous ne pouvons pas nous cacher derri&egrave;re une fa&ccedil;ade ou tromper Dieu. Nous pouvons donc venir en toute libert&eacute; et honn&ecirc;tet&eacute; et Lui dire exactement comment nous nous sentons. Si vous ne vous sentez pas spirituel, dites le Lui. Si votre c&oelig;ur est froid, confessez-le. Si vous avez &eacute;t&eacute; d&eacute;sob&eacute;issant, confessez&nbsp; cela et recevez Son pardon et Sa purification&nbsp;; soyez restaur&eacute; &agrave; communier de nouveau.<br />
La vraie confession est honn&ecirc;te, et implique ce qui suit:</p>

<ul>
	<li>Reconnaitre que notre p&eacute;ch&eacute; est mauvais et est par cons&eacute;quent insupportable pour Dieu.</li>
	<li>Accepter le pardon de Dieu pour nos p&eacute;ch&eacute;s &ndash; pass&eacute;s, pr&eacute;sents et futurs;</li>
	<li>Se repentir, harmoniser notre attitude avec Dieu au sujet du p&eacute;ch&eacute;. Lorsque nous changeons notre attitude, l&rsquo;Esprit Saint nous aide alors &agrave; changer nos actions en cons&eacute;quence.</li>
</ul>

<p>Nous pouvons &ecirc;tre rassur&eacute;s dans notre confession parce que 1 Jean 1:9 promet: &laquo;&nbsp;Si nous confessons nos p&eacute;ch&eacute;s, il est fid&egrave;le et juste pour nous les pardonner, et pour nous purifier de toute iniquit&eacute;.&nbsp;&raquo; M&eacute;fiez-vous des extr&ecirc;mes malsains de confession qui m&egrave;ne &agrave; une introspection inutile. Acceptez le pardon de Dieu pour votre p&eacute;ch&eacute; une fois pour toute, puis concentrez-vous sur Son amour et votre acceptation comme Son enfant.<br />
<br />
Action de gr&acirc;ce. Il n&rsquo;y a aucune meilleure mani&egrave;re de d&eacute;montrer notre foi que de dire, &laquo;&nbsp;Merci Seigneur.&nbsp;&raquo; L&rsquo;auteur du livre des H&eacute;breux dit clairement que&nbsp;; sans la foi il est impossible de lui &ecirc;tre agr&eacute;able (H&eacute;breux 11:6). On nous a recommand&eacute; de rendre gr&acirc;ce en toutes choses car &laquo;&nbsp;c&rsquo;est &agrave; votre &eacute;gard la volont&eacute; de Dieu en J&eacute;sus-Christ.&nbsp;&raquo;<br />
(1 Thessaloniciens 5:18). Ne pas rendre gr&acirc;ce c&rsquo;est d&eacute;sob&eacute;ir Dieu.<br />
<br />
Si nous sommes remplis du Saint-Esprit de Dieu et reconnaissons qu&rsquo;Il contr&ocirc;le toutes choses, nous pouvons Le remercier non seulement pour les b&eacute;n&eacute;dictions de chaque jour, mais aussi pour les probl&egrave;mes et les adversit&eacute;s. Lorsque nous m&eacute;ditons sur la bont&eacute; de Dieu, le salut gratuit qu&rsquo;Il a offert, la vie &eacute;ternelle en Christ, l&rsquo;opportunit&eacute; pour servir, la sant&eacute;, la nourriture, l&rsquo;abri, un pays gratuit ...nous ob&eacute;issons &agrave; l&rsquo;ordre de Dieu. Et la louange a un effet remarquable sur nous. C&rsquo;est revigorant et &eacute;difiant. Si nous focalisons notre attention sur ce que nous avons au lieu de ce que nous voulons, nous pouvons voir la preuve que Dieu est &agrave; l&rsquo;&oelig;uvre en nous.<br />
<br />
Mais louer implique bien s&ucirc;r remercier Dieu pour l&rsquo;adversit&eacute;. Faites la liste de tous les probl&egrave;mes, d&eacute;ception et les chagrins dans votre vie, puis commencer par le haut et remercier Dieu pour chaque entr&eacute;e. On nous recommande de rendre gr&acirc;ce dans l&rsquo;adversit&eacute; comme une d&eacute;monstration de la foi. Exprimer notre foi fait plaisir &agrave; Dieu et Lui permet de manifester Sa force en notre nom. Un esprit critique et incr&eacute;dule, d&rsquo;autre part, d&eacute;plait Le d&eacute;plait, emp&ecirc;che Ses efforts pour nous b&eacute;nir et enrichir nos vies, et l&rsquo;emp&ecirc;che de nous utiliser pour Sa gloire.<br />
<br />
<strong>Supplication. </strong>Paul nous encourage, &laquo;&nbsp;Ne vous inqui&eacute;tez de rien&nbsp;; mais en toute chose faites conna&icirc;tre vos besoins &agrave; Dieu par des pri&egrave;res et des supplications, avec des actions de gr&acirc;ces.&nbsp;&raquo; (Philippiens 4:6). Pour beaucoup de chr&eacute;tiens, la pri&egrave;re est comme une vitrine &mdash; ils passent beaucoup de temps &agrave; regarder, mais ils ne font jamais le choix d&rsquo;acheter. Nous devons connaitre nos c&oelig;urs; nous devons savoir ce dont nous avons besoin, et demander &agrave; Dieu en termes sp&eacute;cifiques, et esp&eacute;rer qu&rsquo;Il r&eacute;ponde.<br />
<br />
La supplication implique, intercession en faveur des autres et les requ&ecirc;tes pour nos propres besoins.<br />
<br />
Nous devons&nbsp; prier pour nos &eacute;pouses, nos enfants et nos parents chaque jour. Nous devons prier pour nos voisins et amis, nos pasteurs et missionnaires, et pour les autres chr&eacute;tiens &agrave; qui Dieu a confi&eacute; une responsabilit&eacute; particuli&egrave;re. Prier pour les autorit&eacute;s.<br />
<br />
Priez sp&eacute;cialement pour le salut des &acirc;mes, les opportunit&eacute;s chaque jour &agrave; introduire d&rsquo;autres &agrave; Christ et au minist&egrave;re du Saint-Esprit, et pour l&rsquo;accomplissement de la Grande Commission dans notre g&eacute;n&eacute;ration. Commencez par votre campus ou votre communaut&eacute;. Priez pour et cherchez un ou plus d&rsquo;amis chr&eacute;tiens avec qui vous pouvez &eacute;tablir des partenariats de pri&egrave;re.<br />
<br />
Les chr&eacute;tiens ne r&eacute;alisent pas souvent l&rsquo;importance de l&rsquo;intercession. L&rsquo;ap&ocirc;tre Paul n&rsquo;a cess&eacute; de prier pour ses convertis (Eph&eacute;siens 1:15-16), et il leur a aussi demand&eacute; de prier pour lui (Eph&eacute;siens 6:19).chaque chr&eacute;tien doit prier pour les autres et doit encourager les autres chr&eacute;tiens &agrave; prier pour lui.<br />
<br />
Nous devons aussi prier pour nous-m&ecirc;mes que notre homme int&eacute;rieur soit r&eacute;v&eacute;l&eacute; et stimul&eacute;, habilit&eacute; par le Saint-Esprit. Nous avons besoin de dire nos probl&egrave;mes &agrave; Dieu et Lui demander la sagesse et l&rsquo;orientation. Nous devons demander avec espoir la force pour r&eacute;sister &agrave; la tentation, et pour le r&eacute;confort dont nous avons besoin dans le chagrin.<br />
Il n&rsquo;y a rien de peu ou de trop grand que nous apporter devant le Seigneur dans la pri&egrave;re. Ce&nbsp; qui est important pour nous l&rsquo;est pour Lui.</p>

<h2>Pouvons-nous prier avec assurance?</h2>

<p>Pouvons-nous esp&eacute;rer des r&eacute;ponses &agrave; nos pri&egrave;res? L&rsquo;Ecriture dit que nous pouvons esp&eacute;rer si nous demeurons, demandons, croyons et recevons.<br />
<br />
J&eacute;sus a r&eacute;v&eacute;l&eacute; que demeurer comme &eacute;tant la cl&eacute; d&rsquo;une pri&egrave;re r&eacute;ussie, prometteuse, &laquo;&nbsp;Si vous demeurez en moi, et que mes paroles demeurent en vous, demandez ce que vous voudrez, et cela vous sera accord&eacute;&nbsp;&raquo; (Jean 15:7).<br />
En d&rsquo;autres mots, si nous Lui confions totalement nos vies&mdash;et Sa Parole demeure en nous en sort que connaissons Sa volont&eacute;&mdash;nous pouvons demander tout ce que nous voulons, car notre d&eacute;sir est de faire Sa volont&eacute;.<br />
<br />
Demeurer signifie simplement marcher selon l&rsquo;Esprit sans un p&eacute;ch&eacute; non confess&eacute; dans nos vies et &ecirc;tre totalement disponible pour Dieu. En priant selon Sa volont&eacute;, nous savons qu&rsquo;Il va nous r&eacute;pondre (1 Jean 5:14).<br />
<br />
Pour esp&eacute;rer des r&eacute;ponses &agrave; nos pri&egrave;res, nous devons demander avec pr&eacute;cision. Jacques dit, &laquo;&nbsp;vous ne poss&eacute;dez pas, parce que vous ne demandez pas.&nbsp;&raquo;&nbsp; Il poursuit pour expliquer, &laquo;&nbsp;Vous demandez, et vous ne recevez pas, parce que vous demandez mal, dans le but de satisfaire vos passions.&nbsp;&raquo; (Jacques 4: 2-3). Le Seigneur J&eacute;sus parle avec l&rsquo;autorit&eacute; de Dieu lorsqu&rsquo;Il dit, &laquo;&nbsp;Si vous demandez quelque chose en mon nom, je le ferai.&nbsp;&raquo; (Jean 14:14).<br />
<br />
J&eacute;sus a promis, &laquo;&nbsp;Tout ce que vous demanderez avec foi par la pri&egrave;re, vous le recevrez.&nbsp;&raquo; (Matthieu 21:22). Croire en Dieu constitue le c&oelig;ur d&rsquo;une pri&egrave;re exauc&eacute;e. Dieu ne demande pas &agrave; ce que nous ayons une grande foi, mais que nous ayons simplement foi en un Dieu grand et digne de foi. J&eacute;sus dit, &laquo;&nbsp;si vous aviez de la foi comme un grain de s&eacute;nev&eacute;, vous diriez &agrave; cette montagne&nbsp;: Transporte-toi d&rsquo;ici l&agrave;, et elle se transporterait&nbsp;; rien ne vous serait impossible.&nbsp;&raquo; (Matthieu 17:20).<br />
<br />
Mais la foi n&rsquo;est pas quelque chose que nous pouvons fabriquer nous-m&ecirc;mes, elle vient de Dieu (Eph&eacute;siens 2:8,9). Le Saint-Esprit produit en nous la foi pendant que nous continuons &agrave; marcher dans l&rsquo;ob&eacute;issance. La foi est comme un muscle&mdash;si nous ne l&rsquo;utilisons pas, nous le perdons.<br />
<br />
Recevez, par la foi, les r&eacute;ponses &agrave; vos requ&ecirc;tes. Si nous sommes respectueux en Christ et sommes dirig&eacute;s par le Saint-Esprit, et si nous prions selon la Parole et la volont&eacute; de Dieu, nous esp&eacute;rer que Dieu r&eacute;ponde &agrave; nos pri&egrave;res. Soyez donc pr&eacute;par&eacute;s &agrave; voir une action. Imaginez que vous recevez les r&eacute;ponses que vous cherchez et commencez par remercier Dieu pour avoir r&eacute;pondu &agrave; votre pri&egrave;re!</p>

<h2>Encore plus de Grandes Choses</h2>

<p>En nous inclinant dans la pri&egrave;re, nous exploitons une source de puissance qui peut changer le cours de l&rsquo;histoire. La puissance, le pouvoir, l&rsquo;amour, la sagesse et la gr&acirc;ce de Dieu sont disponible pour nous si nous croyons en Lui et r&eacute;clamons Sa provision. La pri&egrave;re est le plus grand privil&egrave;ge de l&rsquo;exp&eacute;rience chr&eacute;tienne, parce qu&rsquo;elle nous permet d&rsquo;&ecirc;tre en pr&eacute;sence m&ecirc;me de Dieu. Lorsque nous prenons au s&eacute;rieux les promesses de Dieu, en r&eacute;clamant tout ce qui nous a &eacute;t&eacute; promis, il n&rsquo;y a pas de limite &agrave; ce que Dieu peut faire.<br />
<br />
Si vous souhaitez lib&eacute;rer le plein pouvoir de la pri&egrave;re dans votre vie, rejoignez-moi dans cette pri&egrave;re. :<br />
<br />
<em>P&egrave;re, Tu as dit &laquo;&nbsp;je ne poss&egrave;de pas parce que je ne demande pas.&nbsp;&raquo; Donc, en ce moment je r&eacute;clame Tes promesses, parce que je veux vivre&nbsp; la puissante gloire comme Tu me l&rsquo;as promis, pour Ta gloire. Je prie en Ton puissant nom. Amen.</em></p>

<h2>Application</h2>

<ol>
	<li>Qu&rsquo;avez-vous aim&eacute; le plus (qu&rsquo;est-ce qui a retenu votre attention)?</li>
	<li>Pourquoi?</li>
	<li>A qui devrais-je transmettre cette information ?</li>
</ol>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note1Text')"
        id="note1Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<p>Adapt&eacute; de Les Messages Transmissibles par Bill Bright. &copy; Cru. Tous droits r&eacute;serv&eacute;s</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Comment prier: ', '/content/M2/fra/tc/ct09.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
<!-- end sdcard languageFooterSingle -->

</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->