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
                        <div class="chapter_number ltr"><h1>3.</h1></div>
                        <div class="chapter_title ltr"><h1>Rempli du Saint Esprit</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p><em>Les premiers rayons de la lumi&egrave;re matinale p&eacute;n&eacute;traient la chambre haute par les petites fen&ecirc;tres balay&egrave;rent le visage barbu de Pierre. Il ouvr&icirc;t ses yeux et se redressa sur un coude. La plupart des autres &eacute;taient en &eacute;veil, roulant leurs paillasses et commen&ccedil;ant les pr&eacute;parations du petit d&eacute;jeuner pour encore un nouveau jour. Pendant combien de temps devrait-on patienter encore, Seigneur? Se demandait-il. Ils ont attendu ensemble pendant des jours dans cette petite chambre. Ils sont maintenant plus de 100, attendant juste la venue du Saint-Esprit comme J&eacute;sus l&rsquo;avait promis&hellip;.</em><br />
<br />
<em>Et alors il l&rsquo;entend&icirc;t premi&egrave;rement de loin, Tel un vent imp&eacute;tueux, puis les grondements des vents violents se pr&eacute;cipit&egrave;rent en toute vitesse dans la chambre&nbsp;; r&eacute;sonnant de plus en plus fort&nbsp;; et au milieu d&rsquo;eux des langues de flammes de feu se pos&egrave;rent sur chacun d&rsquo;eux dans la chambre, les remplissant du Saint-Esprit.</em><br />
<br />
Dire que cela a chang&eacute; leurs vies, c&rsquo;est peu dire! Tout &agrave; coup, ces hommes et femmes de Dieu se mirent &agrave; pr&ecirc;cher l&rsquo;&eacute;vangile de J&eacute;sus-Christ avec une nouvelle assurance de sorte que les auditeurs comprirent&nbsp;; ils &eacute;taient m&ecirc;me parvenus &agrave; un point o&ugrave; ils pr&ecirc;ch&egrave;rent dans des langues qu&rsquo;ils n&rsquo;ont jamais apprises! Ils d&eacute;couvrirent une puissance insatiable qui coulait de leur fort int&eacute;rieur parce qu&rsquo;ils avaient &eacute;t&eacute; remplis de la source de la puissance Elle-m&ecirc;me. Et, &agrave; cause de cela, des milliers (de personnes) les suivirent pour une relation nouvelle et transformatrice de vie avec le Seigneur ressuscit&eacute;.<br />
<br />
Le livre des Actes nous rapporte l&rsquo;&oelig;uvre de la puissance du Saint-Esprit dans la vie des gens. Nous lisons les histoires et nous-nous &eacute;merveillons &agrave; la vue des gens ordinaires comme vous et moi faisant des miracles et conduisant des centaines (de personnes) &agrave; Christ. Avec tristesse, nous hochons la t&ecirc;te, d&eacute;&ccedil;us de ce que nous n&rsquo;ayons pas pu vivre en ce temps-l&agrave;, auquel cas nous aurions pu en faire partie int&eacute;grante. Nous avons tout sauf que nous consentons &agrave; l&#39;attitude plus &laquo;&nbsp;sophistiqu&eacute;e&nbsp;&raquo; selon laquelle le Saint-Esprit n&rsquo;&oelig;uvre parmi nous que de mani&egrave;re subtile aujourd&#39;hui. Pierre et les autres devaient faire de miracles pour atteindre les perdus avec l&rsquo;&eacute;vangile. Aujourd&rsquo;hui, beaucoup ne taillent pas d&rsquo;importance &agrave; cette id&eacute;e, disant que ces &laquo;&nbsp;d&eacute;monstrations &eacute;motionnelles&nbsp;&raquo; ne sont plus n&eacute;cessaires.<br />
<br />
Mais J.B. Phillips nous donne plus de d&eacute;tails &agrave; ce propos lorsqu&rsquo;il &eacute;crit dans son introduction &agrave; <em>Lettres aux Jeunes Eglises</em>: &laquo;&nbsp;la grande diff&eacute;rence entre les chr&eacute;tiens d&rsquo;aujourd&rsquo;hui et ceux au sujet desquels nous avons lu dans ces lettres (les &eacute;pitres du Nouveau Testament), est que, pour nous, c&rsquo;est principalement une performance; pour eux, c&rsquo;&eacute;tait une vrai exp&eacute;rience. Nous avons tendance &agrave; r&eacute;duire la religion chr&eacute;tienne &agrave; un code, ou, au mieux, une r&egrave;gle de c&oelig;ur et de vie. Pour ces hommes-l&agrave;, c&rsquo;est tout simplement l&rsquo;invasion de leurs vies par une nouvelle qualit&eacute; de vie enti&egrave;re. Ils n&rsquo;ont pas h&eacute;sit&eacute; &agrave; d&eacute;crire cela comme Christ vivant en eux.&nbsp;&raquo;<br />
<br />
Et si Christ vit toujours en ses disciples comme Il l&rsquo;a promis, nos vies seraient-elles, en quelque point, moins puissantes que celles des disciples? Pour tout chr&eacute;tien, la vie devrait &ecirc;tre une merveilleuse aventure. Nous avons un objectif, et nous avons la source de puissance n&eacute;cessaire pour accomplir les t&acirc;ches qui nous sont &eacute;chues. J&eacute;sus dit, &laquo;&nbsp;celui qui croit en Moi, fera aussi les &oelig;uvres que Je fais et il en fera de plus grandes, parce que Je m&rsquo;en vais au P&egrave;re. Et tout ce que vous demanderez en Mon nom Je le ferai&nbsp;&raquo; (Jean 14:12,13).<br />
<br />
Mais on ne nous demande pas de faire ces choses merveilleuses par notre propre pouvoir. C&rsquo;est Christ Lui-m&ecirc;me vivant en nous qui nous donne le pouvoir de faire &agrave; travers le Saint-Esprit de grandes choses. Toute notre sagesse et &eacute;loquence, toute notre logique, toute notre personnalit&eacute; et nos bonnes apparences ne peuvent jamais persuader quelqu&rsquo;un de suivre Christ, mais par la puissance de la r&eacute;surrection de J&eacute;sus, Son c&oelig;ur, Sa pens&eacute;e, Son amour pour les perdus qui coulent de notre fort int&eacute;rieur, qui pouvait r&eacute;sister?<br />
<br />
&nbsp;Si nous ne pouvons pas voir la manifestation de la puissance du Saint-Esprit dans nos vies, il nous faut faire le bilan et nous demander si nous vivons comme des chr&eacute;tiens charnels. Si ce n&rsquo;est pas le cas, la raison de l&rsquo;absence de la puissance est peut &ecirc;tre un manque de foi, ou un manque de connaissance au sujet de qui&nbsp; Dieu et Son Esprit Saint sont.<br />
<br />
<em>Il y a quelques ann&eacute;es un fermier, originaire de l&rsquo;Ouest de l&rsquo;&eacute;tat du Texas a f&icirc;t une d&eacute;couverte surprenante.</em><br />
<br />
<em>L&#39;histoire raconte que pour Homer Yates, la fin de la route semblait &ecirc;tre venue trop t&ocirc;t. Comme il faisait reposer une botte poussi&eacute;reuse sur le marchepied de&nbsp; son pick-up us&eacute;, il regarda de l&rsquo;autre c&ocirc;t&eacute; de la ferme qui s&rsquo;&eacute;tendait sur des hectares parsem&eacute;e de grappes de bovins. Cette vall&eacute;e &eacute;tait sa vall&eacute;e. Sa famille et lui avaient appel&eacute; cette terre leur maison pendant d&rsquo;innombrables ann&eacute;es.</em><br />
<em>&nbsp;&nbsp; </em><br />
<em>Cette sc&egrave;ne famili&egrave;re lui a autrefois amen&eacute; la paix du c&oelig;ur. Elle le confortait. Mais cette fois-ci elle le fit fondre en larmes. Il aimait cet endroit. Comment pouvait-il le laisser derri&egrave;re lui? Comment pouvait-il s&rsquo;attendre &agrave;&nbsp; ranger ses affaires et s&rsquo;en aller de la ferme pour laquelle il s&rsquo;&eacute;tait inverti corps et &acirc;me pendant tant d&rsquo;ann&eacute;es?</em><br />
<br />
<em>Et pourtant, quel autre choix avait-il maintenant?</em><br />
<br />
<em>Les choses allaient bien jusqu&rsquo;&agrave; ce que la crise frappa. Elle est venue comme un essaim de sauterelles d&eacute;vorantes et l&rsquo;a d&eacute;pouill&eacute; financi&egrave;rement. Il avait m&ecirc;me d&ucirc; accepter la subvention du gouvernement pour pouvoir faire fonctionner un temps soit peu sa ferme qu&rsquo;il affectionnait tant. C&rsquo;&eacute;tait pour lui une&nbsp; honte de demander de l&rsquo;aide&mdash;mais il ne semblait pas y avoir d&rsquo;autre alternative. Et aussi soigneusement que sa femme et lui r&eacute;partissaient leur maigres ressources financi&egrave;res, ils n&rsquo;en avaient jamais assez. Ils &eacute;taient dans le manque, ils avaient sacrifi&eacute; tout ce qu&rsquo;il &eacute;tait possible de sacrifier, mais la ruine fut leur r&eacute;compense.</em><br />
<br />
<em>Maintenant, il aper&ccedil;&ucirc;t de loin un autre camion qui venait par la rue rocailleuse avec &agrave; bord quelques hommes qui lui &eacute;taient inconnus. Ils s&rsquo;arr&ecirc;t&egrave;rent &agrave; quelques m&egrave;tres au loin, avec des tourbillons de poussi&egrave;re qui montait autour d&rsquo;eux pendant qu&rsquo;ils s&rsquo;approchaient de lui.</em><br />
<br />
<em>&laquo;&nbsp;C&rsquo;est vous Yates?,&nbsp;&raquo; demanda l&rsquo;un d&rsquo;eux. Il r&eacute;pondit de la t&ecirc;te. &laquo;&nbsp;Nous vous cherchions,&nbsp;&raquo; dit-il, surprenant Yates avec une poign&eacute;e de main. Le plus &eacute;lanc&eacute; expliqua qu&rsquo;ils faisaient partie d&rsquo;une &eacute;quipe de g&eacute;ologues envoy&eacute;e par une importante compagnie p&eacute;troli&egrave;re, et qu&rsquo;ils avaient des raisons de croire qu&rsquo;il y aurait du p&eacute;trole sur sa terre, et s&rsquo;il leur permettrait de forer un puits de p&eacute;trole de l&rsquo;autre c&ocirc;t&eacute; de la montagne?</em><br />
<br />
<em>Qu&rsquo;avait-il &agrave; perdre? Il signa le bail cet apr&egrave;s-midi-l&agrave;. A un peu moins de 1100 pieds ils trouv&egrave;rent une r&eacute;serve de p&eacute;trole qui produisait 80,000 barils par jour avant que Yates ne se rende compte de ce qui lui arrivait. Plusieurs d&rsquo;entre les puits qui ont suivi rapportaient le double de cette quantit&eacute;. Et Yates et sa famille poss&eacute;daient tout cela!</em><br />
<br />
<em>Du jour au lendemain, le modeste fermier, &agrave; la merci du gouvernement, &eacute;tait devenu un multimillionnaire (en dollars am&eacute;ricain). Il a v&eacute;cu dans la pauvret&eacute; sur cette m&ecirc;me terre qui l&rsquo;a rendu riche. Les r&eacute;serves de p&eacute;trole ont toujours &eacute;t&eacute; l&agrave; tout ce temps &mdash;tout &agrave; lui depuis le jour qu&rsquo;il a sign&eacute; le contrat. Mais il ne les a poss&eacute;d&eacute;s qu&rsquo;apr&egrave;s avoir compris quelles richesses se trouvaient l&agrave;, et qu&rsquo;il ne lui restait qu&rsquo;&agrave; prendre.</em></p>

<h2>Id&eacute;es fausses</h2>

<p>Combien de fois nous en tant que chr&eacute;tiens, ne faisons-nous pas la m&ecirc;me chose, vivant comme des indigents spirituels alors qu&rsquo;en v&eacute;rit&eacute;, nous sommes des enfants du Roi! J&eacute;sus a d&eacute;crit la vie chr&eacute;tienne comme une aventure passionnante, abondante, et pendant des si&egrave;cles beaucoup de croyants de par le monde l&rsquo;ont trouv&eacute; vrai.<br />
<br />
Un autre probl&egrave;me que nous avons est que nous crayons que Dieu profite de nous d&rsquo;une mani&egrave;re ou d&rsquo;une autre si nous nous donnons compl&egrave;tement &agrave; Lui. Nous voyons dans 1 Jean 4:18, &laquo;&nbsp;La crainte n&rsquo;est pas dans l&rsquo;amour, mais l&rsquo;amour parfait bannit la crainte&nbsp;; car la crainte suppose un ch&acirc;timent, et celui qui craint n&rsquo;est pas parfait dans l&rsquo;amour.&nbsp;&raquo; (LSG). Nous pouvons faire confiance &agrave; Dieu avec nos vies une fois que nous commen&ccedil;ons &agrave; accepter Son amour.<br />
<br />
Imaginez un instant avec moi que vous &ecirc;tes le parent d&rsquo;un petit gar&ccedil;on que vous aimez profond&eacute;ment. Un jour chaud d&rsquo;&eacute;t&eacute; il se tient sur vos genoux et a du mal &agrave; vous dire quelque chose d&rsquo;une grande importance pour lui. &laquo;&nbsp;Je t&rsquo;aime,&nbsp;&raquo; dit-il finalement, en tapotant votre main, et &agrave; partir de maintenant je vais faire tout ce que tu me demandes de faire. Vous vous mettez &agrave; genou &agrave; c&ocirc;t&eacute; de lui, tenant ses petites &eacute;paules dans vos mains, vous commencez par le secouer violemment. Vous verrez ses yeux remplis de terreur pendant que vous criez, &laquo;&nbsp;Je n&rsquo;attendais que cela! Maintenant je vais rendre les choses mis&eacute;rables pour toi. Plus d&rsquo;amusement, plus de jouets, rien que de corv&eacute;es odieuses et horribles pour tout le temps que tu vivras!&nbsp;&raquo;</p>

<p><br />
Quelle &eacute;trange r&eacute;ponse de la part d&rsquo;un parent qui aime.&nbsp;! Nous devons nous attendre &agrave; voir une manifestation de la tendresse et de la compassion envers l&rsquo;enfant, et non une tirade comme celle-ci. Et pourtant, nous avons si souvent peur d&rsquo;une pareille r&eacute;ponse douloureuse et punitive de la part de Dieu si nous osons nous abandonner &agrave; Lui. Un parent humain ouvrirait ses bras &agrave; son petit, l&rsquo;accueillant m&ecirc;me au plus profond de son intimit&eacute;. Il s&rsquo;attendrait &agrave; m&eacute;riter un tel amour de la part de son enfant.<br />
<br />
Pourquoi esp&eacute;rons-nous alors quelque chose de moins de la part de Dieu qui nous aime au-del&agrave; de l&rsquo;amour humain? C&rsquo;est parce que nous ne comprenons pas Son amour pour nous? Matthieu 7:11 d&eacute;crit Dieu comme un p&egrave;re qui d&eacute;montre son amour pour ses enfants: &laquo;&nbsp;Si donc, m&eacute;chants comme vous l&rsquo;&ecirc;tes, vous savez donner de bonnes choses &agrave; vos enfants, &agrave; combien plus forte raison votre P&egrave;re qui est dans les cieux donnera-t-il de bonnes choses &agrave; ceux qui les lui demandent!&nbsp;&raquo;<br />
<br />
Comme J&eacute;sus qui pleura sur J&eacute;rusalem, Dieu nous regarde et dit, &laquo; combien de fois ai-je voulu vous rassembler, comme une poule rassemble ses poussins sous ses ailes, et vous ne l&rsquo;avez pas voulu&nbsp;!&nbsp;&raquo; Si nous voulons &ecirc;tre des chr&eacute;tiens efficaces nous devons commencer&mdash;par la foi&mdash;&agrave; faire confiance au Dieu de notre salut. Depuis le moment o&ugrave; nous acceptons Son pardon jusqu&rsquo; au moment o&ugrave; Il marche avec nous &agrave; travers la mort, toute chose qu&rsquo;Il nous donne nous la recevons par la foi.</p>

<h2>La Respiration Spirituelle</h2>

<p>Dans &laquo;&nbsp;Comment vivre l&rsquo;Amour et le Pardon de Dieu,&nbsp;&raquo; nous avons abord&eacute; le principe de la &laquo;&nbsp;respiration spirituelle,&nbsp;&raquo; en d&eacute;finissant &laquo;&nbsp;expiration&nbsp;&raquo; comme la confession de p&eacute;ch&eacute; et la reconnaissance de l&rsquo;amour et le pardon de Dieu dans nos vies. Nous venons maintenant &agrave; l&rsquo;&laquo;&nbsp;inspiration.&nbsp;&raquo;<br />
<br />
La respiration spirituelle serait incompl&egrave;te sans le processus de l&rsquo;&laquo;&nbsp;inspiration&nbsp;&raquo; comme il le serait de la respiration physique. Lorsque la respiration est obstru&eacute;e et emp&ecirc;che l&rsquo;oxyg&egrave;ne de parvenir aux poumons, aux cerveaux et aux organes vitaux, le corps humain meurt. Une bonne respiration spirituelle est de la m&ecirc;me importance dramatique. &laquo;&nbsp;Inspirer&nbsp;&raquo; spirituellement c&rsquo;est prendre profond&eacute;ment de la fraicheur du Saint-Esprit, en s&rsquo;appropriant par la foi Sa pl&eacute;nitude, Lui permettant de r&eacute;gner librement dans nos vies afin de nous diriger et nous habiliter comme Il le veut.</p>

<p><br />
A mesure que nous pratiquons la respiration spirituelle, cela devient une habitude. Une &laquo;&nbsp;expiration&nbsp;&raquo; constante et rythmique&nbsp;&raquo; (confession) et une &laquo;&nbsp;inspiration&nbsp;&raquo; (appropriation de nouvelle puissance dans nos vies) cr&eacute;ent une approche quotidienne fraiche et incomparable &agrave; la vie.</p>

<h2>L&rsquo;Esprit Saint</h2>

<p>Mais si nous devons Lui soumettre nos vies, nous devons commencer avec une compr&eacute;hension de la nature et de la personne du Saint-Esprit. Vous remarquerez que je ne m&rsquo;&eacute;tais pas r&eacute;f&eacute;r&eacute; &agrave; Lui comme une &laquo; chose.&nbsp;&raquo; le Saint-Esprit est autant une personne qu&rsquo;IL est Dieu. Il n&rsquo;est&nbsp; pas une influence immat&eacute;rielle ou un concept&nbsp; spirituel blanc comme la laine. Il est Dieu. Il poss&egrave;de tous les attributs qui sont imput&eacute;s &agrave; Dieu le P&egrave;re. En tant que troisi&egrave;me personne de la trinit&eacute;, l&rsquo;Esprit Saint est &eacute;gal &agrave; Dieu le P&egrave;re et &agrave; Dieu le Fils. Il y a un seul Dieu, mais Il se manifeste en trois personnes. D&eacute;finir la trinit&eacute;, n&rsquo;est pas du ressort des humains. Un de mes professeurs au s&eacute;minaire a l&rsquo;habitude de dire &laquo;&nbsp;Celui qui renie la trinit&eacute; perdra son &acirc;me. Celui qui essaie de comprendre la trinit&eacute; perdra sa raison.&nbsp;&raquo; L&rsquo;homme limit&eacute; ne peut totalement comprendre l&rsquo;infinit&eacute; de Dieu.<br />
<br />
C&rsquo;est l&rsquo;Esprit Saint qui a inspir&eacute; les hommes pour &eacute;crire les Ecritures. Pendant que nous lisons la Bible, c&rsquo;est Lui qui nous r&eacute;v&egrave;le sa v&eacute;rit&eacute; et nous aide &agrave; comprendre comment l&rsquo;appliquer &agrave; nos vies. Il fait entendre nos pri&egrave;res par Dieu, et c&rsquo;est Lui qui&nbsp; moissonne les fruits de notre fid&egrave;le t&eacute;moignage. Son seul but est d&rsquo;exalter et de glorifier Christ (Jean 16:1-15).<br />
<br />
La preuve de l&rsquo;&oelig;uvre du Saint-Esprit dans la vie des croyants est tout autour de nous. Il est venu &agrave; nous, le Consolateur que J&eacute;sus a promis pendant qu&rsquo;Il se pr&eacute;parait &agrave; quitter cette terre. &laquo;&nbsp;Cependant je vous dis la v&eacute;rit&eacute;: il vous est avantageux que je m&rsquo;en aille, car si je ne m&rsquo;en vais pas, le consolateur ne viendra pas vers vous&nbsp;; mais, si je m&rsquo;en vais, je vous l&rsquo;enverrai&hellip; Quand le consolateur sera venu, l&rsquo;Esprit de v&eacute;rit&eacute;, il vous conduira dans toute la v&eacute;rit&eacute;&nbsp;; car il ne parlera pas de lui-m&ecirc;me, mais il dira tout ce qu&rsquo;il aura entendu, et il vous annoncera les choses &agrave; venir. Il me glorifiera, parce qu&rsquo;il prendra de ce qui est &agrave; moi, et vous l&rsquo;annoncera.&nbsp;&raquo; (Jean 16:7, 13, 14). Par la nouvelle naissance le Saint-Esprit nous permet de connaitre Christ, et de partager la Bonne Nouvelle avec les autres.<br />
<br />
1 Jean 1:7 dit, &laquo;&nbsp;Mais si nous marchons dans la lumi&egrave;re, comme il est lui-m&ecirc;me dans la lumi&egrave;re, nous sommes mutuellement en communion, et le sang de J&eacute;sus son Fils nous purifie de tout p&eacute;ch&eacute;.&nbsp;&raquo; Quand nous sommes remplis de l&rsquo;Esprit, nous sommes sous Son contr&ocirc;le; pas comme un robot mais comme quelqu&rsquo;un qui est conduit et habilit&eacute; par le c&oelig;ur de Dieu Lui-m&ecirc;me. Il marche ici-bas dans nos corps, en vivant Sa vie de r&eacute;surrection en nous et par nous.<br />
<br />
J&eacute;sus dit &agrave; la multitude, &laquo;&nbsp;Si quelqu&rsquo;un a soif, qu&rsquo;il vienne &agrave; moi, et qu&rsquo;il boive. Celui qui croit en moi, des fleuves d&rsquo;eau vive couleront de son sein, comme dit l&rsquo;Ecriture.&nbsp;&raquo; (Jean 7: 37,38). Jean ajoute, &laquo;&nbsp;Il dit cela de l&rsquo;Esprit que devaient recevoir ceux qui croiraient en lui&nbsp;&raquo; (Jean 7:39). Nous pouvons vivre la vie victorieuse et remplie de puissance que J&eacute;sus offre si nous ouvrons nos c&oelig;urs au Saint-Esprit pour qu&rsquo;Il habite en nous. A nous le choix.</p>

<h2>Le Saint-Esprit est en vous</h2>

<p>Mais une question se pose: <em>Comment?</em> Comment permettons-nous au Saint-Esprit de nous diriger? Que faisons-nous, que disons-nous, pour qu&rsquo;Il puisse prendre le contr&ocirc;le en nous ou bien pour que nous puissions avoir acc&egrave;s &agrave; cette merveilleuse puissance qui est la n&ocirc;tre?<br />
<br />
Supposons que vous avez un compte bancaire contenant plusieurs milliers de dollars, et vous avez besoin d&rsquo;encaisser un ch&egrave;que. Irez-vous &agrave; la banque vous agenouiller devant un caissier, et commen&ccedil;ant &agrave; le supplier et plaider pour l&rsquo;argent dont vous avez besoin? Vous souriez parce que vous savez que le caissier, surpris, va s&ucirc;rement se pencher vers le comptoir et vous rappeler ceci&nbsp;:&nbsp;&laquo;&nbsp;Vous n&rsquo;avez pas &agrave; me supplier. C&rsquo;est d&eacute;j&agrave; votre argent. Ecrivez simplement ce que vous voulez, et je vais encaisser votre ch&egrave;que.&nbsp;&raquo;<br />
<br />
Le Saint-Esprit nous est donn&eacute; le jour o&ugrave; nous acceptons le pardon de Christ pour les p&eacute;ch&eacute;s. Comme le salut, la pl&eacute;nitude du Saint-Esprit est un acte de foi. &laquo;&nbsp;Car c&rsquo;est par la gr&acirc;ce que vous &ecirc;tes sauv&eacute;s, par le moyen de la foi. Et cela ne vient pas de vous, c&rsquo;est le don de Dieu.&nbsp;&raquo;, &laquo;&nbsp;Ce n&rsquo;est point par les &oelig;uvres, afin que personne ne se glorifie.&nbsp;&raquo; (Eph&eacute;siens 2:8,9).<br />
<br />
Nous n&rsquo;avons pas besoin de supplier Dieu ou faire de troc avec Lui pour b&eacute;n&eacute;ficier de Sa faveur. Je&ucirc;ner, pleurer, nous prosterner devant Dieu, jamais rien de cela n&rsquo;am&egrave;nera Dieu &agrave; nous remplir de Son Esprit. Nous ne pouvons pas gagner la pl&eacute;nitude de Dieu. Elle est &agrave; nous seulement par la foi et elle a &eacute;t&eacute; n&ocirc;tre depuis le moment o&ugrave; nous sommes devenus chr&eacute;tiens. Colossiens 2:6 nous rappelle, &laquo;&nbsp;Ainsi donc, comme vous avez re&ccedil;u le Seigneur J&eacute;sus-Christ, marchez en Lui.&nbsp;&raquo;</p>

<h2>Appropriez-vous la Puissance du Saint-Esprit</h2>

<p>Le Saint-Esprit est &agrave; nous. Ce que nous devons apprendre &agrave; faire maintenant est de nous approprier Sa puissance. Il y a plusieurs facteurs qui vont nous aider &agrave; pr&eacute;parer nos c&oelig;urs &agrave; mesure que nous cherchons &agrave; avoir des vies remplies du Saint-Esprit.<br />
<br />
Nous devons avoir faim de l&rsquo;Esprit et d&eacute;sirer qu&rsquo;Il habite en nous.<br />
<br />
J&eacute;sus dit,&nbsp;&laquo;&nbsp;Heureux ceux qui ont faim et soif de la justice, car ils seront rassasi&eacute;s&nbsp;&raquo; (Matthieu 5:6).<br />
<br />
Nous devons souhaiter ardemment soumettre nos vies &agrave; Christ. Dans Romains 12:1,2 Paul &eacute;crit, &laquo;&nbsp;Je vous exhorte donc, fr&egrave;res, par les compassions de Dieu, &agrave; offrir vos corps comme un sacrifice vivant, saint, agr&eacute;able &agrave; Dieu, ce qui sera de votre part un culte raisonnable. Ne vous conformez pas au si&egrave;cle pr&eacute;sent, mais soyez transform&eacute;s par le renouvellement de l&rsquo;intelligence, afin que vous discerniez quelle est la volont&eacute; de Dieu, ce qui est bon, agr&eacute;able et parfait.&nbsp;&raquo; (LSG).<br />
<br />
Confessez tout p&eacute;ch&eacute;. Nous devons laisser le Saint-Esprit nous rappeler tout ce qui doit &ecirc;tre r&eacute;gl&eacute;, puis tout confesser &agrave; Dieu. Il nous est promis dans 1 Jean 1:9: &laquo;&nbsp;Si nous confessons nos p&eacute;ch&eacute;s, il est fid&egrave;le et juste pour nous les pardonner, et pour nous purifier de toute iniquit&eacute;.. (Et il est parfaitement convenable pour Dieu de faire cela pour nous parce que Christ est mort pour laver nos p&eacute;ch&eacute;s)&nbsp;&raquo; (LSG).<br />
<br />
Avec les c&oelig;urs ouverts et pr&eacute;par&eacute;s pour &ecirc;tre remplis du Saint-Esprit, nous sommes instruits dans Eph&eacute;siens 5:18 &agrave; ne pas &laquo;&nbsp;&ecirc;tre enivrer du vin, c&rsquo;est de la d&eacute;bauche, mais &agrave; &ecirc;tre remplis du Saint-Esprit.&nbsp;&raquo; C&rsquo;est un ordre! Ne pas &ecirc;tre rempli, dirig&eacute; et habilit&eacute;, c&rsquo;est de la d&eacute;sob&eacute;issance. L&rsquo;Ecriture nous dit aussi que &laquo;&nbsp;nous avons aupr&egrave;s de Lui cette assurance que si nous demandons quelque chose selon Sa volont&eacute;, Il nous &eacute;coute. Et si nous savons qu&rsquo;il nous &eacute;coute, quelque chose que nous demandions, nous savons que nous poss&eacute;dons la chose que nous lui avons demand&eacute;e&nbsp;&raquo;. (I Jean 5:14,15).<br />
<br />
Il n&rsquo;y a qu&rsquo;une seule pr&eacute;sence int&eacute;rieure, une seule nouvelle naissance, et un seul bapt&ecirc;me du Saint-Esprit &mdash;tout ceci se produit au moment du salut. Il y a plusieurs mani&egrave;res d&rsquo;&ecirc;tre rempli qui sont claires dans Eph&eacute;siens 5:18. Dans le texte original, le sens est plus explicite que la plupart des traductions Fran&ccedil;aises1. Ce commandement signifie &ecirc;tre constamment et continuellement rempli, dirig&eacute; et habilit&eacute; par le Saint-Esprit comme un mode de vie!<br />
<br />
Techniquement, nous ne devons m&ecirc;me pas prier pour &ecirc;tre rempli du Saint-Esprit puisqu&rsquo;aucune Ecriture ne nous demande de faire cela. Nous sommes remplis par la foi. Cependant, puisque l&rsquo;objet de notre foi est Dieu et Sa Parole, nous pouvons prier comme une expression de notre foi en le commandement de Dieu et en Sa promesse. Nous ne sommes pas remplis parce que nous prions mais parce que nous avons confiance en Dieu qui r&eacute;pond &agrave; notre foi.<br />
<br />
Est-ce cela le d&eacute;sir de votre c&oelig;ur? Si vous le voulez, faites cette pri&egrave;re:</p>

<blockquote><em>&laquo;&nbsp;Cher P&egrave;re, je reconnais que j&#39;ai &eacute;t&eacute; le ma&icirc;tre de ma vie, et par cons&eacute;quent, j&#39;ai d&eacute;sob&eacute;i &agrave; Ton commandement d&#39;&ecirc;tre dirig&eacute; par l&#39;Esprit.</em><br />
<em>&nbsp;Merci de m&rsquo;avoir pardonn&eacute;, et maintenant, P&egrave;re j&rsquo;invite Christ &agrave; prendre Sa place l&eacute;gitime sur le tr&ocirc;ne de ma vie. Par la foi je te demande de me remplir de Ton Esprit Saint comme Tu l&rsquo;as promis dans Ta Parole. Merci d&#39;avoir tenu Tes promesses et pour la pr&eacute;sence permanente du Saint-Esprit dans ma vie maintenant.&nbsp;&raquo; </em></blockquote>

<p>Si vous avez fait cette pri&egrave;re ou exprim&eacute; votre c&oelig;ur d&rsquo;une telle mani&egrave;re &agrave; Dieu avec vos propres mots, vous &ecirc;tes &agrave; pr&eacute;sent remplis du Saint-Esprit. Vous n&rsquo;avez besoin d&rsquo;en avoir le&nbsp; &laquo;&nbsp;sentiment&nbsp;&raquo;; croyez-le simplement comme un fait&mdash;par la foi. Vous pouvez d&egrave;s ce moment commencer &agrave; faire usage des vastes et in&eacute;puisables ressources du Saint-Esprit. Il vous rendra capable de vivre une vie sainte, de partager les d&eacute;clarations de Christ t avec tout votre c&oelig;ur, ceci, d&rsquo;une nouvelle mani&egrave;re.<br />
<br />
Remerciez Dieu pour la pl&eacute;nitude de Son Esprit chaque matin, et continuez &agrave; L&rsquo;inviter moment apr&egrave;s moment &agrave; diriger votre vie. La vie remplie de l&rsquo;Esprit est une vie de puissance surnaturelle, durable en Christ, et qui porte de fruit spirituel. C&rsquo;est avoir confiance en Dieu, et non en soi, pour vivre la vie chr&eacute;tienne.</p>

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

			<td class="social" @click="share('lesson', 'Rempli du Saint Esprit: ', '/content/M2/fra/tc/ct03.html')">
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