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
                        <div class="chapter_number ltr"><h1>5.</h1></div>
                        <div class="chapter_title ltr"><h1>Témoigner par l'Esprit</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p>&laquo;&nbsp;C&rsquo;&eacute;tait affreux,&nbsp;&raquo; dit-il, secouant tristement sa t&ecirc;te. &laquo;&nbsp;Je viens d&rsquo;&ecirc;tre congel&eacute;.<br />
Juste au moment o&ugrave; je devrais lui pr&eacute;senter l&rsquo;&eacute;vangile, j&rsquo;ai oubli&eacute; toutes choses que j&rsquo;ai eu &agrave; entendre au sujet de comment conduire un ami &agrave; Christ. C&rsquo;&eacute;tait si g&ecirc;nant, si inconfortable &hellip; pour nous les deux&nbsp;&raquo; Il mit ses mains dans les poches de sa jeans, &laquo;&nbsp;je pense que j&rsquo;ai vraiment tout g&acirc;ch&eacute; cette fois!&nbsp;&raquo;<br />
<br />
Sans doute mon jeune ami frustr&eacute; est en train d&rsquo;exprimer un des sentiments que nous tous nous avons eus lorsque nous essayons de conduire quelqu&rsquo;un &agrave; Christ. C&rsquo;est sans doute, l&rsquo;exp&eacute;rience la plus importante dans la vie d&rsquo;une personne. Mais si nous ne sommes pas pr&eacute;par&eacute;s,&nbsp; cela peut nous causer beaucoup de d&eacute;sarroi et de malaise inutile.<br />
<br />
Les perdus ont faim de J&eacute;sus-Christ, mais la majorit&eacute; des chr&eacute;tiens n&rsquo;ont jamais conduit une autre &acirc;me &agrave; Christ. Cela est d&ucirc; &agrave; deux raisons fondamentales: La premi&egrave;re, le Chr&eacute;tien ordinaire ne vit pas une vie victorieuse dirig&eacute;e par l&rsquo;Esprit; la seconde, la plupart ne savent pas comment communiquer leur foi en Christ aux autres d&rsquo;une mani&egrave;re efficace.<br />
<br />
Si vous avez &eacute;t&eacute; au rang de ceux qui ont le d&eacute;sir de partager Christ mais n&rsquo;avez pas &eacute;t&eacute; aussi productifs comme vous le souhaitiez, le plan de t&eacute;moignage &eacute;tabli sur les quelques pages qui suivent vous sera d&rsquo;un int&eacute;r&ecirc;t vital. Si vous le prenez &agrave; c&oelig;ur et le mettez en pratique, il vous aidera &agrave; vous approprier le r&ocirc;le actif, participatif et fructueux que vous d&eacute;siriez dans votre contact de tous les jours avec les gens. Il est constitu&eacute; de huit &eacute;tapes simples, con&ccedil;ues pour vous aider &agrave; devenir un t&eacute;moin qui porte de fruit.</p>

<h2>1. Soyez s&ucirc;r que vous &ecirc;tes un chr&eacute;tien.</h2>

<p>Quelqu&rsquo;un qui veut introduire d&rsquo;autres &agrave; Christ ne peut &ecirc;tre utilis&eacute; effacement &agrave; moins qu&rsquo;il soit d&rsquo;abord devenu lui-m&ecirc;me un chr&eacute;tien. Vous devez&nbsp; &ecirc;tre s&ucirc;r&nbsp; que vous avez&nbsp; invit&eacute; J&eacute;sus-Christ &agrave; &ecirc;tre le Seigneur et Sauveur de votre vie. C&rsquo;est la premi&egrave;re et la plus indispensable &eacute;tape. C&rsquo;est par l&agrave; que commence la marche chr&eacute;tienne.</p>

<h2>2. Confessez tout p&eacute;ch&eacute; dans votre vie.</h2>

<p>Nous devons &ecirc;tre s&ucirc;rs qu&rsquo;il n&rsquo;y a pas de p&eacute;ch&eacute; non confess&eacute; dans nos vies, parce que le p&eacute;ch&eacute; nous s&eacute;pare de Dieu. Nous nous mettons &agrave; jour &agrave; ce sujet lorsque nous continuons par respirer spirituellement&mdash;&laquo;&nbsp;expiration&nbsp;&raquo; pour expulser le p&eacute;ch&eacute; par une confession r&eacute;guli&egrave;re &agrave; Dieu.</p>

<h2>3. Soyez remplis du Saint-Esprit</h2>

<p>Il est imp&eacute;ratif que nous soyons remplis du Saint-Esprit, &laquo;&nbsp;inspirer&nbsp;&raquo; spirituellement d&rsquo;une mani&egrave;re constante pour s&rsquo;approprier &agrave; nouveau la puissance illimit&eacute;e qu&rsquo;Il met &agrave; la disposition de Ses enfants.</p>

<h2>4. Soyez pr&eacute;par&eacute;s &agrave; partager votre foi.</h2>

<p>Nous devons nous pr&eacute;parer &agrave; partager notre foi en Christ avec d&rsquo;autres&nbsp; en toute occasion. Nos s&eacute;minaires et &eacute;coles bibliques font un travail formidable pour pr&eacute;parer les chr&eacute;tiens &agrave; pr&eacute;senter l&rsquo;&eacute;vangile de J&eacute;sus-Christ de mani&egrave;re efficace et dynamique dans le monde entier.&nbsp; Toutefois chacun de nous peut esp&eacute;rer &ecirc;tre utilis&eacute; selon Dieu o&ugrave; que nous soyons, avec rien d&rsquo;autre que la connaissance que nous avons eu aujourd&rsquo;hui.<br />
<br />
Lorsque nous mettons ensemble un c&oelig;ur dispos&eacute; et la puissance que donne le Saint-Esprit, des &acirc;mes sont gagn&eacute;es &agrave; Christ. Un t&eacute;moignage qui touche les c&oelig;urs des perdus ne d&eacute;pend pas d&rsquo;une formation professionnelle. L&rsquo;&eacute;vangile de J&eacute;sus-Christ est assez simple &agrave; saisir pour tout enfant, et nous n&rsquo;avons pas besoin des dipl&ocirc;mes en th&eacute;ologie avant d&rsquo;aider les gens &agrave; connaitre Christ personnellement.<br />
<br />
J&eacute;sus dit, &laquo;&nbsp;Tout pouvoir m&rsquo;a &eacute;t&eacute; donn&eacute; dans le ciel et sur la terre&nbsp;&raquo;. Et puis Il nous recommande, &laquo;&nbsp;Allez, faites de toutes les nations des disciples, les baptisant au nom du P&egrave;re, du Fils et du Saint-Esprit, et enseignez-leur &agrave; observer tout ce que je vous ai prescrit&nbsp;&raquo; (Matthieu 28: 18-20). Mais Il ne nous envoie&nbsp; jamais seuls. Les derni&egrave;res paroles du livre de Matthieu sont une promesse douce pour tous les chr&eacute;tiens. J&eacute;sus dit &laquo;&nbsp;Et voici, je suis avec vous tous les jours, jusqu&rsquo;&agrave; la fin du monde.&nbsp;&raquo;<br />
<br />
Aussi surprenant que cela puisse paraitre, Dieu a choisi de limiter l&rsquo;expression de Son amour aux &ecirc;tres humains ici sur Sa terre. Il n&rsquo;a d&rsquo;autres armes que nous, autre c&oelig;ur que nous, aucune voix que celle de Ses enfants. Nous constituons une partie vitale de Son plan pour atteindre le reste du monde avec Son amour. Nous sommes des &laquo;&nbsp;porteurs&nbsp;&raquo;. Alors notre responsabilit&eacute; est de Le suivre; et c&rsquo;est &agrave; Lui de faire de nous des t&eacute;moins efficaces. Si nous sommes ob&eacute;issants, Il va beaucoup nous utiliser dans cette aventure passionnante pour gagner le monde!</p>

<h2>5. N&rsquo;oubliez pas de prier.</h2>

<p>Il faut que nous priions pour ceux que nous esp&eacute;rons voir venir &agrave; Christ. La Bible nous dit que Dieu ne veut pas qu&rsquo;aucun p&eacute;risse, mais que tous arrivent &agrave; la repentance. &laquo;&nbsp;Le Seigneur ne tarde pas dans l&rsquo;accomplissement de la promesse, comme quelques-uns le croient&nbsp;; mais Il use de patience envers vous, ne voulant pas qu&rsquo;aucun p&eacute;risse, mais voulant que tous arrivent &agrave; la repentance.&nbsp;&raquo; (2 Pierre 3:9, LSG). Il promet aussi que si nous demandons quelque chose selon Sa volont&eacute;, Il va nous &eacute;couter et nous r&eacute;pondre. &laquo;&nbsp;Nous avons aupr&egrave;s de Lui cette assurance, que si nous demandons quelque chose selon sa volont&eacute;, il nous &eacute;coute. Et si nous savons qu&rsquo;il nous &eacute;coute, quelque chose que nous demandions, nous savons que nous poss&eacute;dons la chose que nous Lui avons demand&eacute;e.&nbsp;&raquo;&nbsp; (1 Jean 5: 14,15, LSG). La promesse ne veut pas dire que toute personne qui &eacute;coute l&rsquo;&eacute;vangile va suivre Christ,&nbsp; mais il n&rsquo;y a aucun moyen de dire qui choisira Christ et qui Le rejettera. Bien qu&rsquo;il y a des gens qui vont entendre l&rsquo;&eacute;vangile et choisir de s&rsquo;en aller, c&rsquo;est notre responsabilit&eacute; &mdash;et privil&egrave;ge &mdash; de prier pour les perdus parce que Dieu honore nos pri&egrave;res.<br />
<br />
Commencez par faire la liste en nommant ceux que le Saint-Esprit vous met &agrave; c&oelig;ur. Puis pr&eacute;sentez les &agrave; Dieu de fa&ccedil;on quotidienne; vous avez l&rsquo;autorit&eacute; de le faire sur la base de ce que les Ecritures ont mentionn&eacute; ci-dessus. Continuez par partager de toute mani&egrave;re possible l&rsquo;amour de J&eacute;sus en priant. Nous ne sommes pas toujours capables de parler de l&rsquo;&eacute;vangile; nous sommes parfois limit&eacute;s &agrave;&nbsp; le vivre silencieusement, mais nous pouvons &ecirc;tre s&ucirc;rs que les semences sont en train d&rsquo;&ecirc;tre mises &agrave; terre et que l&rsquo;Esprit est &agrave; l&rsquo;&oelig;uvre! Puisque les non sauv&eacute;s se rendent compte de votre amour sans int&eacute;r&ecirc;t &agrave; leur endroit, le Saint-Esprit &oelig;uvra dans leurs c&oelig;urs, en les attirant vers Lui-m&ecirc;me dans le temps.<br />
<br />
Parfois il nous est permis de partager la joie de ceux pour qui nous prions lorsqu&rsquo;ils donnent leurs vies &agrave; Christ. Cela peut prendre des ann&eacute;es pour d&rsquo;autres de devenir chr&eacute;tiens. D&rsquo;autres peuvent toujours paraitre &laquo;&nbsp;sans espoir&nbsp;&raquo; &agrave; nos yeux en refusant d&rsquo;accepter une quelconque part du christianisme. Ne perdez pas espoir. Dieu &oelig;uvre d&rsquo;une mani&egrave;re insoup&ccedil;onnable. Priez simplement, et laissez le Seigneur s&rsquo;occuper du r&eacute;sultat.</p>

<h2>6. Aller parler de Christ aux autres.</h2>

<p>Nous n&rsquo;allons pas attendre que des hommes viennent &agrave; nous. Nous pouvons et devons leur apporter la Bonne Nouvelle. Mais l&rsquo;un des obstacles les plus difficiles dans le t&eacute;moignage est de commencer. Satan aimes nous remplir des excuses: C&rsquo;est que je suis juste pris maintenant, ou je ne sais vraiment pas ce qu&rsquo;il faut dire &agrave; quelqu&rsquo;un au sujet de Christ. Pourtant, nous ne sommes pas seuls. Le Saint-Esprit marche avec nous. En fait, Il nous pr&eacute;c&egrave;de dans chaque pas, pr&eacute;parant les c&oelig;urs des gens &agrave; qui nous parlerons. J&eacute;sus nous a dit d&rsquo;annoncer la Bonne Nouvelle &agrave; tous les hommes. Nous pouvons compter sur Lui pour nous soutenir et nous donner la force pendant que nous faisons ce qu&rsquo;Il nous a demand&eacute;s de faire.</p>

<h2>7. Parler de Christ.</h2>

<p>Paul dit, &laquo;&nbsp;C&rsquo;est lui que nous annon&ccedil;ons, exhortant tout homme, et instruisant tout homme en toute sagesse, afin de pr&eacute;senter &agrave; Dieu tout homme, devenu parfait en Christ.&nbsp;&raquo; (Colossiens 1:28, LSG). Paul nous a &eacute;tabli un pr&eacute;c&eacute;dent &agrave; suivre, mais il &eacute;tait sensible au choix de son auditeur d&rsquo;&eacute;couter. Il ne for&ccedil;ait pas l&rsquo;&eacute;vangile. Il y a aura des gens qui semblent insister pour rester sur un niveau superficiel avec nous, et qui refusent d&rsquo;ouvrir leurs oreilles leurs c&oelig;urs &agrave; la Bonne Nouvelle. Bien que cela puisse &ecirc;tre frustrant, nous devons &ecirc;tre sensibles &agrave; la direction du Saint-Esprit et &agrave; la recherche de son Timing. Il dirigera et mettra les occasions disponibles comme bon Lui semble.<br />
<br />
Quand j&#39;&eacute;tais juste un gar&ccedil;on, ma famille avait l&#39;habitude de visiter la maison de mon oncle &agrave; la campagne. Pendant des kilom&egrave;tres avant que nous ne prenions l&#39;all&eacute;e sinueuse et rocailleuse menant &agrave; la grande et vieille maison blanche, je pouvais sentir le parfum all&eacute;chant des p&ecirc;ches grasses et juteuses qui soufflaient &agrave; travers les fen&ecirc;tres ouvertes. Quelques minutes apr&egrave;s notre arriv&eacute;e, ma tante Sara m&#39;envoyait mon cousin et moi dans le verger pour remplir un panier de boisseau entre nous, et nous reviendrions des heures plus tard, le panier et nos ventres bomb&eacute;s et remplis &agrave; d&eacute;border.<br />
<br />
Cela ne m&rsquo;a pas pris assez de temps pour comprendre que les meilleures p&ecirc;ches &agrave; cueillir &mdash; et &agrave; manger &mdash; &eacute;taient les m&ucirc;res! Nous avons laiss&eacute; le fruit vert sur les arbres jusqu&#39;&agrave; ce que nous soyons de nouveau envoy&eacute;s au verger pour remplir un autre panier. J&#39;ai trop t&ocirc;t d&eacute;couvert que quelque chose de merveilleux s&#39;&eacute;tait pass&eacute; en notre absence. Le fruit que nous avions laiss&eacute; sur les arbres parce qu&#39;il &eacute;tait vert et dur &eacute;tait devenu joufflu et juteux, juste parfait pour l&#39;un des cordonniers divins de Tante Sara.<br />
<br />
La m&ecirc;me chose est vraie pour le t&eacute;moignage. Nous devons &ecirc;tre sensible &agrave; la &laquo;&nbsp;maturit&eacute;&nbsp;&raquo; du c&oelig;ur qui re&ccedil;oit notre t&eacute;moignage.&nbsp; Certains seront pr&ecirc;ts la premi&egrave;re fois qu&rsquo;ils entendent. D&rsquo;autres auront besoin de temps, et plus de pri&egrave;re, avant de recevoir Christ dans leur vie. Ce n&rsquo;est pas notre responsabilit&eacute; de leur mettre la pression pour qu&rsquo;ils se d&eacute;cident pour Christ. Envisagez leur laisser&nbsp; une litt&eacute;rature bien choisie, et restez ouverts &agrave; la direction du Saint-Esprit pour&nbsp; parler avec eux&nbsp; plus tard. Comme ceux qui sont pr&ecirc;ts &agrave; consid&eacute;rer les d&eacute;clarations&nbsp; du Christ s&#39;ouvrent &agrave; votre t&eacute;moignage, souvenez-vous de les encourager &agrave; L&#39;inviter dans leurs vies. Beaucoup de c&oelig;urs sont pr&ecirc;ts &agrave; Le recevoir mais sont ignorant de comment devenir un croyant. Des conseils doux et sensibles, souvent accompagn&eacute;s d&#39;une aide comme la brochure des Quatre Lois Spirituelles, leur montreront, &eacute;tape par &eacute;tape, comment retourner leur c&oelig;ur au contr&ocirc;le de Dieu.. Cette brochure aide aussi &agrave; garder la conversation centr&eacute;e sur Christ sans se laisser d&eacute;tourner par des questions de distraction.</p>

<h2>8. Esp&eacute;rer que le c&oelig;ur r&eacute;ponde &agrave; l&rsquo;&eacute;vangile.</h2>

<p>Nous pouvons avoir confiance en la puissance du Dieu de la cr&eacute;ation. Il est souverain. Il est omnipotent. Et Il ne veut pas qu&rsquo;aucun p&eacute;risse. Comme les vendeurs qui n&#39;ont jamais eu &agrave; vendre du porte-&agrave;-porte, certains chr&eacute;tiens approchent les perdus avec une attitude de vous ne serez pas int&eacute;ress&eacute;s &agrave; devenir chr&eacute;tien d&egrave;s le d&eacute;part. Nous n&rsquo;avons pas &agrave; avoir honte de rien. Le Seigneur de nos vies est le Seigneur de tous, le Roi des rois! Nous devons t&eacute;moigner avec un esprit d&rsquo;esp&eacute;rance. Dieu nous devance pour pr&eacute;parer les c&oelig;urs, pour les faire m&ucirc;rir en Son temps. Il y a ceux qui attendent sans Christ et qui d&eacute;sirent Le trouver.<br />
<br />
Satan, le &laquo;&nbsp;p&egrave;re du mensonge,&nbsp;&raquo; veut nous faire croire que les gens ne sont pas int&eacute;ress&eacute;s &agrave; trouver Dieu. Nous nous sommes permis de nous tromper en pensant que les c&oelig;urs ne seront pas sensibles &agrave; l&#39;&eacute;vangile. Mais aujourd&rsquo;hui nous vivons des moments critiques et passionnants! Le Saint-Esprit &oelig;uvre parmi les &eacute;tudiants et les la&iuml;cs dans le monde entier. Les gens viennent &agrave; Christ r&eacute;guli&egrave;rement et en masse. Il y a une soif de J&eacute;sus-Christ, l&rsquo;eau vive (Jean 4: 10-15).<br />
<br />
Pas d&rsquo;erreur, ce n&rsquo;est pas la religion que les hommes et les femmes cherchent aujourd&rsquo;hui. Pour la plupart, ils ne veulent rien &agrave; avoir avec l&rsquo;&eacute;glise et des r&egrave;gles organis&eacute;es selon lesquelles ils vont vivre. Ce qu&#39;ils veulent en fait, c&#39;est l&#39;exp&eacute;rience d&#39;une relation r&eacute;elle et vitale avec le Sauveur. La religion c&rsquo;est la recherche de Dieu par l&rsquo;homme. Le christianisme est beaucoup plus: C&rsquo;est la r&eacute;v&eacute;lation de Dieu Lui-m&ecirc;me &agrave; l&rsquo;homme &agrave; travers la personne de J&eacute;sus-Christ. Si, dans l&#39;amour, nous confrontons les gens aux d&eacute;clarations de Christ, nous verrons beaucoup de gens r&eacute;pondre &agrave; Son amour et &agrave; Son pardon. Mais la responsabilit&eacute; de leur d&eacute;cision&nbsp; repose sur le Saint-Esprit.<br />
<br />
Nous, au Campus Pour Christ, croyons sinc&egrave;rement que le succ&egrave;s dans le t&eacute;moignage est simplement&nbsp; <em>partager Christ dans la puissance du Saint-Esprit et laisser Dieu s&rsquo;occuper des r&eacute;sultats</em>.<br />
<br />
Apprenez ces directives faciles &agrave; suivre pour t&eacute;moigner dans l&#39;Esprit. Mettez-les en pratique dans votre vie et observez les r&eacute;sultats. Si vous vous &ecirc;tes assis sur le banc de touche du t&eacute;moignage en regardant les autres gagner des gens &agrave; Christ, cela va changer votre vie ... et la vie de ceux qui entendent l&#39;Evangile &agrave; cause de vous!</p>

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

			<td class="social" @click="share('lesson', 'Témoigner par l\'Esprit: ', '/content/M2/fra/tc/ct05.html')">
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