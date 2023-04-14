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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply1-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>9.</h1></div>
                        <div class="chapter_title ltr"><h1>Les Personnes préparées par Dieu</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="back">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

<ul>
	<li>Exemple: Lisez <span class="popup-link" @click = "popUp('pop1')"> Romains 11:33-36</span>&nbsp;&nbsp;et ex&eacute;cutez 1-2 chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">33&nbsp;</sup>O profondeur de la richesse, de la sagesse et de la science de Dieu! Que ses jugements sont insondables, et ses voies incompr&eacute;hensibles! Car</p>

	<p><sup class="versenum">34&nbsp;</sup>Qui a connu la pens&eacute;e du Seigneur, Ou qui a &eacute;t&eacute; son conseiller?</p>

	<p><sup class="versenum">35&nbsp;</sup>Qui lui a donn&eacute; le premier, pour qu&#39;il ait &agrave; recevoir en retour?</p>

	<p><sup class="versenum">36&nbsp;</sup>C&#39;est de lui, par lui, et pour lui que sont toutes choses. A lui la gloire dans tous les si&egrave;cles! Amen!</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<ul>
</ul>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Dieu change les vies et les utilise pour Sa gloire. Un exemple est l&#39;histoire d&#39;un homme du Moyen-Orient nomm&eacute; Adam. Il a &eacute;t&eacute; form&eacute; pour &ecirc;tre un martyr pour sa religion. Mais tout cela a chang&eacute; une nuit lorsqu&rsquo;il a rencontr&eacute; Christ de fa&ccedil;on dramatique. Il &eacute;tait tellement enthousiasm&eacute; par sa nouvelle relation avec Christ, qu&rsquo;il a commenc&eacute; &agrave; t&eacute;moigner &agrave; tous ceux qu&#39;il connaissait. Malgr&eacute; sa pers&eacute;cution, il continue de partager l&#39;&Eacute;vangile et de former les autres. Encouragez-les en lisant<span class="popup-link" @click = "popUp('pop2')">  1 Corinthiens 1: 24-31</span>.</p>

<div class="popup invisible" id="pop2"><!-- begin bible -->
<p><sup class="versenum">24&nbsp;</sup>mais puissance de Dieu et sagesse de Dieu pour ceux qui sont appel&eacute;s, tant Juifs que Grecs.</p>

<p><sup class="versenum">25&nbsp;</sup>Car la folie de Dieu est plus sage que les hommes, et la faiblesse de Dieu est plus forte que les hommes.</p>

<p><sup class="versenum">26&nbsp;</sup>Consid&eacute;rez, fr&egrave;res, que parmi vous qui avez &eacute;t&eacute; appel&eacute;s il n&#39;y a ni beaucoup de sages selon la chair, ni beaucoup de puissants, ni beaucoup de nobles.</p>

<p><sup class="versenum">27&nbsp;</sup>Mais Dieu a choisi les choses folles du monde pour confondre les sages; Dieu a choisi les choses faibles du monde pour confondre les fortes;</p>

<p><sup class="versenum">28&nbsp;</sup>et Dieu a choisi les choses viles du monde et celles qu&#39;on m&eacute;prise, celles qui ne sont point, pour r&eacute;duire &agrave; n&eacute;ant celles qui sont,</p>

<p><sup class="versenum">29&nbsp;</sup>afin que nulle chair ne se glorifie devant Dieu.</p>

<p><sup class="versenum">30&nbsp;</sup>Or, c&#39;est par lui que vous &ecirc;tes en J&eacute;sus Christ, lequel, de par Dieu, a &eacute;t&eacute; fait pour nous sagesse, justice et sanctification et r&eacute;demption,</p>

<p><sup class="versenum">31&nbsp;</sup>afin, comme il est &eacute;crit, Que celui qui se glorifie se glorifie dans le Seigneur.</p>
<!-- end bible --></div>
&nbsp;</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ Contexte</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>J&eacute;sus a mis au d&eacute;fi quatre hommes de le suivre et d&#39;apprendre &agrave; p&ecirc;cher des hommes. Alors que J&eacute;sus entra&icirc;nait ses disciples &agrave; p&ecirc;cher des hommes, il leur a donn&eacute; le mod&egrave;le de six situations diff&eacute;rentes. La derni&egrave;re situation &eacute;tait par rapport &agrave; un fonctionnaire du gouvernement improbable qui rejoindrait les quatre hommes et deviendrait l&#39;un des disciples les plus proches de J&eacute;sus.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 5:27-32 deux fois pendant que tout le monde &eacute;coute.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 5:27-32</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">27&nbsp;</sup>Apr&egrave;s cela, J&eacute;sus sortit, et il vit un publicain, nomm&eacute; L&eacute;vi, assis au lieu des p&eacute;ages. Il lui dit: Suis-moi.</p>

<p><sup class="versenum">28&nbsp;</sup>Et, laissant tout, il se leva, et le suivit.</p>

<p><sup class="versenum">29&nbsp;</sup>L&eacute;vi lui donna un grand festin dans sa maison, et beaucoup de publicains et d&#39;autres personnes &eacute;taient &agrave; table avec eux.</p>

<p><sup class="versenum">30&nbsp;</sup>Les pharisiens et les scribes murmur&egrave;rent, et dirent &agrave; ses disciples: Pourquoi mangez-vous et buvez-vous avec les publicains et les gens de mauvaise vie?</p>

<p><sup class="versenum">31&nbsp;</sup>J&eacute;sus, prenant la parole, leur dit: Ce ne sont pas ceux qui se portent bien qui ont besoin de m&eacute;decin, mais les malades.</p>

<p><sup class="versenum">32&nbsp;</sup>Je ne suis pas venu appeler &agrave; la repentance des justes, mais des p&eacute;cheurs.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/109.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 5:27-39&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (passage)?</li>
</ul>

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


<h2>Lire, raconter et corriger</h2>

<ul>
	<li>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Lisez <span class="popup-link" @click = "popUp('pop3')"> Luc 10: 1-11</span>.&nbsp;</p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">1 </sup>Apr&egrave;s cela, le Seigneur d&eacute;signa encore soixante-dix autres disciples, et il les envoya deux &agrave; deux devant lui dans toutes les villes et dans tous les lieux o&ugrave; lui-m&ecirc;me devait aller.</p>

<p><sup class="versenum">2&nbsp;</sup>Il leur dit: La moisson est grande, mais il y a peu d&#39;ouvriers. Priez donc le ma&icirc;tre de la moisson d&#39;envoyer des ouvriers dans sa moisson.</p>

<p><sup class="versenum">3&nbsp;</sup>Partez; voici, je vous envoie comme des agneaux au milieu des loups.</p>

<p><sup class="versenum">4&nbsp;</sup>Ne portez ni bourse, ni sac, ni souliers, et ne saluez personne en chemin.</p>

<p><sup class="versenum">5&nbsp;</sup>Dans quelque maison que vous entriez, dites d&#39;abord: Que la paix soit sur cette maison!</p>

<p><sup class="versenum">6&nbsp;</sup>Et s&#39;il se trouve l&agrave; un enfant de paix, votre paix reposera sur lui; sinon, elle reviendra &agrave; vous.</p>

<p><sup class="versenum">7&nbsp;</sup>Demeurez dans cette maison-l&agrave;, mangeant et buvant ce qu&#39;on vous donnera; car l&#39;ouvrier m&eacute;rite son salaire. N&#39;allez pas de maison en maison.</p>

<p><sup class="versenum">8&nbsp;</sup>Dans quelque ville que vous entriez, et o&ugrave; l&#39;on vous recevra, mangez ce qui vous sera pr&eacute;sent&eacute;,</p>

<p><sup class="versenum">9&nbsp;</sup>gu&eacute;rissez les malades qui s&#39;y trouveront, et dites-leur: Le royaume de Dieu s&#39;est approch&eacute; de vous.</p>

<p><sup class="versenum">10&nbsp;</sup>Mais dans quelque ville que vous entriez, et o&ugrave; l&#39;on ne vous recevra pas, allez dans ses rues, et dites:</p>

<p><sup class="versenum">11&nbsp;</sup>Nous secouons contre vous la poussi&egrave;re m&ecirc;me de votre ville qui s&#39;est attach&eacute;e &agrave; nos pieds; sachez cependant que le royaume de Dieu s&#39;est approch&eacute;.</p>
<!-- end bible --></div>

<p>&nbsp;J&eacute;sus a envoy&eacute; ses disciples faire les m&ecirc;mes choses qu&#39;Il faisait: prier pour les gens, prendre soin de leurs besoins et parler du Royaume. Cela peut &ecirc;tre r&eacute;sum&eacute; comme pri&egrave;re, soin, t&eacute;moignage. Il s&#39;est multipli&eacute; en formant et en envoyant de nouveaux ouvriers. L&rsquo;homme de Paix est une personne pr&eacute;par&eacute;e par Dieu qui vous recevra et recevra votre message. A travers leurs relations, ils ouvrent de nouveaux r&eacute;seaux de personnes &agrave; l&#39;&eacute;vangile.</p>

</div>

<div class="for-enrichment">
<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude plus approfondie: &Eacute;tudiez les hommes de paix suivants et discutez avec un autre membre du groupe: <span class="popup-link" @click = "popUp('pop4')"> Luc 19: 1-10</span>,&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>J&eacute;sus, &eacute;tant entr&eacute; dans J&eacute;richo, traversait la ville.</p>

	<p><sup class="versenum">2&nbsp;</sup>Et voici, un homme riche, appel&eacute; Zach&eacute;e, chef des publicains, cherchait &agrave; voir qui &eacute;tait J&eacute;sus;</p>

	<p><sup class="versenum">3&nbsp;</sup>mais il ne pouvait y parvenir, &agrave; cause de la foule, car il &eacute;tait de petite taille.</p>

	<p><sup class="versenum">4&nbsp;</sup>Il courut en avant, et monta sur un sycomore pour le voir, parce qu&#39;il devait passer par l&agrave;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Lorsque J&eacute;sus fut arriv&eacute; &agrave; cet endroit, il leva les yeux et lui dit: Zach&eacute;e, h&acirc;te-toi de descendre; car il faut que je demeure aujourd&#39;hui dans ta maison.</p>

	<p><sup class="versenum">6&nbsp;</sup>Zach&eacute;e se h&acirc;ta de descendre, et le re&ccedil;ut avec joie.</p>

	<p><sup class="versenum">7&nbsp;</sup>Voyant cela, tous murmuraient, et disaient: Il est all&eacute; loger chez un homme p&eacute;cheur.</p>

	<p><sup class="versenum">8&nbsp;</sup>Mais Zach&eacute;e, se tenant devant le Seigneur, lui dit: Voici, Seigneur, je donne aux pauvres la moiti&eacute; de mes biens, et, si j&#39;ai fait tort de quelque chose &agrave; quelqu&#39;un, je lui rends le quadruple.</p>

	<p><sup class="versenum">9&nbsp;</sup>J&eacute;sus lui dit: Le salut est entr&eacute; aujourd&#39;hui dans cette maison, parce que celui-ci est aussi un fils d&#39;Abraham.</p>

	<p><sup class="versenum">10&nbsp;</sup>Car le Fils de l&#39;homme est venu chercher et sauver ce qui &eacute;tait perdu.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop5')"> Marc 5: 14-20</span>,&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Ceux qui les faisaient pa&icirc;tre s&#39;enfuirent, et r&eacute;pandirent la nouvelle dans la ville et dans les campagnes. Les gens all&egrave;rent voir ce qui &eacute;tait arriv&eacute;.</p>

	<p><sup class="versenum">15&nbsp;</sup>Ils vinrent aupr&egrave;s de J&eacute;sus, et ils virent le d&eacute;moniaque, celui qui avait eu la l&eacute;gion, assis, v&ecirc;tu, et dans son bon sens; et ils furent saisis de frayeur.</p>

	<p><sup class="versenum">16&nbsp;</sup>Ceux qui avaient vu ce qui s&#39;&eacute;tait pass&eacute; leur racont&egrave;rent ce qui &eacute;tait arriv&eacute; au d&eacute;moniaque et aux pourceaux.</p>

	<p><sup class="versenum">17&nbsp;</sup>Alors ils se mirent &agrave; supplier J&eacute;sus de quitter leur territoire.</p>

	<p><sup class="versenum">18&nbsp;</sup>Comme il montait dans la barque, celui qui avait &eacute;t&eacute; d&eacute;moniaque lui demanda la permission de rester avec lui.</p>

	<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus ne le lui permit pas, mais il lui dit: Va dans ta maison, vers les tiens, et raconte-leur tout ce que le Seigneur t&#39;a fait, et comment il a eu piti&eacute; de toi.</p>

	<p><sup class="versenum">20&nbsp;</sup>Il s&#39;en alla, et se mit &agrave; publier dans la D&eacute;capole tout ce que J&eacute;sus avait fait pour lui. Et tous furent dans l&#39;&eacute;tonnement.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop6')"> Jean 4: 1-42</span>,&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Le Seigneur sut que les pharisiens avaient appris qu&#39;il faisait et baptisait plus de disciples que Jean.</p>

	<p><sup class="versenum">2&nbsp;</sup>Toutefois J&eacute;sus ne baptisait pas lui-m&ecirc;me, mais c&#39;&eacute;taient ses disciples.</p>

	<p><sup class="versenum">3&nbsp;</sup>Alors il quitta la Jud&eacute;e, et retourna en Galil&eacute;e.</p>

	<p><sup class="versenum">4&nbsp;</sup>Comme il fallait qu&#39;il pass&acirc;t par la Samarie,</p>

	<p><sup class="versenum">5&nbsp;</sup>il arriva dans une ville de Samarie, nomm&eacute;e Sychar, pr&egrave;s du champ que Jacob avait donn&eacute; &agrave; Joseph, son fils.</p>

	<p><sup class="versenum">6&nbsp;</sup>L&agrave; se trouvait le puits de Jacob. J&eacute;sus, fatigu&eacute; du voyage, &eacute;tait assis au bord du puits. C&#39;&eacute;tait environ la sixi&egrave;me heure.</p>

	<p><sup class="versenum">7&nbsp;</sup>Une femme de Samarie vint puiser de l&#39;eau. J&eacute;sus lui dit: Donne-moi &agrave; boire.</p>

	<p><sup class="versenum">8&nbsp;</sup>Car ses disciples &eacute;taient all&eacute;s &agrave; la ville pour acheter des vivres.</p>

	<p><sup class="versenum">9&nbsp;</sup>La femme samaritaine lui dit: Comment toi, qui es Juif, me demandes-tu &agrave; boire, &agrave; moi qui suis une femme samaritaine? -Les Juifs, en effet, n&#39;ont pas de relations avec les Samaritains. -</p>

	<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Si tu connaissais le don de Dieu et qui est celui qui te dit: Donne-moi &agrave; boire! tu lui aurais toi-m&ecirc;me demand&eacute; &agrave; boire, et il t&#39;aurait donn&eacute; de l&#39;eau vive.</p>

	<p><sup class="versenum">11&nbsp;</sup>Seigneur, lui dit la femme, tu n&#39;as rien pour puiser, et le puits est profond; d&#39;o&ugrave; aurais-tu donc cette eau vive?</p>

	<p><sup class="versenum">12&nbsp;</sup>Es-tu plus grand que notre p&egrave;re Jacob, qui nous a donn&eacute; ce puits, et qui en a bu lui-m&ecirc;me, ainsi que ses fils et ses troupeaux?</p>

	<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Quiconque boit de cette eau aura encore soif;</p>

	<p><sup class="versenum">14&nbsp;</sup>mais celui qui boira de l&#39;eau que je lui donnerai n&#39;aura jamais soif, et l&#39;eau que je lui donnerai deviendra en lui une source d&#39;eau qui jaillira jusque dans la vie &eacute;ternelle.</p>

	<p><sup class="versenum">15&nbsp;</sup>La femme lui dit: Seigneur, donne-moi cette eau, afin que je n&#39;aie plus soif, et que je ne vienne plus puiser ici.</p>

	<p><sup class="versenum">16&nbsp;</sup>Va, lui dit J&eacute;sus, appelle ton mari, et viens ici.</p>

	<p><sup class="versenum">17&nbsp;</sup>La femme r&eacute;pondit: Je n&#39;ai point de mari. J&eacute;sus lui dit: Tu as eu raison de dire: Je n&#39;ai point de mari.</p>

	<p><sup class="versenum">18&nbsp;</sup>Car tu as eu cinq maris, et celui que tu as maintenant n&#39;est pas ton mari. En cela tu as dit vrai.</p>

	<p><sup class="versenum">19&nbsp;</sup>Seigneur, lui dit la femme, je vois que tu es proph&egrave;te.</p>

	<p><sup class="versenum">20&nbsp;</sup>Nos p&egrave;res ont ador&eacute; sur cette montagne; et vous dites, vous, que le lieu o&ugrave; il faut adorer est &agrave; J&eacute;rusalem.</p>

	<p><sup class="versenum">21&nbsp;</sup>Femme, lui dit J&eacute;sus, crois-moi, l&#39;heure vient o&ugrave; ce ne sera ni sur cette montagne ni &agrave; J&eacute;rusalem que vous adorerez le P&egrave;re.</p>

	<p><sup class="versenum">22&nbsp;</sup>Vous adorez ce que vous ne connaissez pas; nous, nous adorons ce que nous connaissons, car le salut vient des Juifs.</p>

	<p><sup class="versenum">23&nbsp;</sup>Mais l&#39;heure vient, et elle est d&eacute;j&agrave; venue, o&ugrave; les vrais adorateurs adoreront le P&egrave;re en esprit et en v&eacute;rit&eacute;; car ce sont l&agrave; les adorateurs que le P&egrave;re demande.</p>

	<p><sup class="versenum">24&nbsp;</sup>Dieu est Esprit, et il faut que ceux qui l&#39;adorent l&#39;adorent en esprit et en v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">25&nbsp;</sup>La femme lui dit: Je sais que le Messie doit venir (celui qu&#39;on appelle Christ); quand il sera venu, il nous annoncera toutes choses.</p>

	<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus lui dit: Je le suis, moi qui te parle.</p>

	<p><sup class="versenum">27&nbsp;</sup>L&agrave;-dessus arriv&egrave;rent ses disciples, qui furent &eacute;tonn&eacute;s de ce qu&#39;il parlait avec une femme. Toutefois aucun ne dit: Que demandes-tu? ou: De quoi parles-tu avec elle?</p>

	<p><sup class="versenum">28&nbsp;</sup>Alors la femme, ayant laiss&eacute; sa cruche, s&#39;en alla dans la ville, et dit aux gens:</p>

	<p><sup class="versenum">29&nbsp;</sup>Venez voir un homme qui m&#39;a dit tout ce que j&#39;ai fait; ne serait-ce point le Christ?</p>

	<p><sup class="versenum">30&nbsp;</sup>Ils sortirent de la ville, et ils vinrent vers lui.</p>

	<p><sup class="versenum">31&nbsp;</sup>Pendant ce temps, les disciples le pressaient de manger, disant: Rabbi, mange.</p>

	<p><sup class="versenum">32&nbsp;</sup>Mais il leur dit: J&#39;ai &agrave; manger une nourriture que vous ne connaissez pas.</p>

	<p><sup class="versenum">33&nbsp;</sup>Les disciples se disaient donc les uns aux autres: Quelqu&#39;un lui aurait-il apport&eacute; &agrave; manger?</p>

	<p><sup class="versenum">34&nbsp;</sup>J&eacute;sus leur dit: Ma nourriture est de faire la volont&eacute; de celui qui m&#39;a envoy&eacute;, et d&#39;accomplir son oeuvre.</p>

	<p><sup class="versenum">35&nbsp;</sup>Ne dites-vous pas qu&#39;il y a encore quatre mois jusqu&#39;&agrave; la moisson? Voici, je vous le dis, levez les yeux, et regardez les champs qui d&eacute;j&agrave; blanchissent pour la moisson.</p>

	<p><sup class="versenum">36&nbsp;</sup>Celui qui moissonne re&ccedil;oit un salaire, et amasse des fruits pour la vie &eacute;ternelle, afin que celui qui s&egrave;me et celui qui moissonne se r&eacute;jouissent ensemble.</p>

	<p><sup class="versenum">37&nbsp;</sup>Car en ceci ce qu&#39;on dit est vrai: Autre est celui qui s&egrave;me, et autre celui qui moissonne.</p>

	<p><sup class="versenum">38&nbsp;</sup>Je vous ai envoy&eacute;s moissonner ce que vous n&#39;avez pas travaill&eacute;; d&#39;autres ont travaill&eacute;, et vous &ecirc;tes entr&eacute;s dans leur travail.</p>

	<p><sup class="versenum">39&nbsp;</sup>Plusieurs Samaritains de cette ville crurent en J&eacute;sus &agrave; cause de cette d&eacute;claration formelle de la femme: Il m&#39;a dit tout ce que j&#39;ai fait.</p>

	<p><sup class="versenum">40&nbsp;</sup>Aussi, quand les Samaritains vinrent le trouver, ils le pri&egrave;rent de rester aupr&egrave;s d&#39;eux. Et il resta l&agrave; deux jours.</p>

	<p><sup class="versenum">41&nbsp;</sup>Un beaucoup plus grand nombre crurent &agrave; cause de sa parole;</p>

	<p><sup class="versenum">42&nbsp;</sup>et ils disaient &agrave; la femme: Ce n&#39;est plus &agrave; cause de ce que tu as dit que nous croyons; car nous l&#39;avons entendu nous-m&ecirc;mes, et nous savons qu&#39;il est vraiment le Sauveur du monde.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop7')"> Actes 16: 13-15</span>.

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">13&nbsp;</sup>Le jour du sabbat, nous nous rend&icirc;mes, hors de la porte, vers une rivi&egrave;re, o&ugrave; nous pensions que se trouvait un lieu de pri&egrave;re. Nous nous ass&icirc;mes, et nous parl&acirc;mes aux femmes qui &eacute;taient r&eacute;unies.</p>

	<p><sup class="versenum">14&nbsp;</sup>L&#39;une d&#39;elles, nomm&eacute;e Lydie, marchande de pourpre, de la ville de Thyatire, &eacute;tait une femme craignant Dieu, et elle &eacute;coutait. Le Seigneur lui ouvrit le coeur, pour qu&#39;elle f&ucirc;t attentive &agrave; ce que disait Paul.</p>

	<p><sup class="versenum">15&nbsp;</sup>Lorsqu&#39;elle eut &eacute;t&eacute; baptis&eacute;e, avec sa famille, elle nous fit cette demande: Si vous me jugez fid&egrave;le au Seigneur, entrez dans ma maison, et demeurez-y. Et elle nous pressa par ses instances.</p>
	<!-- end bible --></div>
	</li>
</ul>
</div>

<div class="forward">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<ul>
	<li>R&eacute;visez en utilisant la question fascinante et prendre soin des autres.</li>
	<li>Pratiquez toute comp&eacute;tence ou sujet des le&ccedil;ons pr&eacute;c&eacute;dentes si n&eacute;cessaire.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<p>o Utilisez ce que vous avez appris cette semaine avec au moins 3</p>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note2Text')"
        id="note2Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la Mission</h2>

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</li>
</ul>

<p>&nbsp;</p>
</div>
</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Les Personnes préparées par Dieu: ', '/content/M2/fra/multiply1/multiply109.html')">
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