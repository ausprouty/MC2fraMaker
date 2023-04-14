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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>33.</h1></div>
                        <div class="chapter_title ltr"><h1>Des personnes de paix dans des lieux improbables</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 16:16-40 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 16:16-40</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">16&nbsp;</sup>Comme nous allions au lieu de pri&egrave;re, une servante qui avait un esprit de Python, et qui, en devinant, procurait un grand profit &agrave; ses ma&icirc;tres, vint au-devant de nous,</p>

<p><sup class="versenum">17&nbsp;</sup>et se mit &agrave; nous suivre, Paul et nous. Elle criait: Ces hommes sont les serviteurs du Dieu Tr&egrave;s Haut, et ils vous annoncent la voie du salut.</p>

<p><sup class="versenum">18&nbsp;</sup>Elle fit cela pendant plusieurs jours. Paul fatigu&eacute; se retourna, et dit &agrave; l&#39;esprit: Je t&#39;ordonne, au nom de J&eacute;sus Christ, de sortir d&#39;elle. Et il sortit &agrave; l&#39;heure m&ecirc;me.</p>

<p><sup class="versenum">19&nbsp;</sup>Les ma&icirc;tres de la servante, voyant dispara&icirc;tre l&#39;espoir de leur gain, se saisirent de Paul et de Silas, et les tra&icirc;n&egrave;rent sur la place publique devant les magistrats.</p>

<p><sup class="versenum">20&nbsp;</sup>Ils les pr&eacute;sent&egrave;rent aux pr&eacute;teurs, en disant: Ces hommes troublent notre ville;</p>

<p><sup class="versenum">21&nbsp;</sup>ce sont des Juifs, qui annoncent des coutumes qu&#39;il ne nous est permis ni de recevoir ni de suivre, &agrave; nous qui sommes Romains.</p>

<p><sup class="versenum">22&nbsp;</sup>La foule se souleva aussi contre eux, et les pr&eacute;teurs, ayant fait arracher leurs v&ecirc;tements, ordonn&egrave;rent qu&#39;on les batt&icirc;t de verges.</p>

<p><sup class="versenum">23&nbsp;</sup>Apr&egrave;s qu&#39;on les eut charg&eacute;s de coups, ils les jet&egrave;rent en prison, en recommandant au ge&ocirc;lier de les garder s&ucirc;rement.</p>

<p><sup class="versenum">24&nbsp;</sup>Le ge&ocirc;lier, ayant re&ccedil;u cet ordre, les jeta dans la prison int&eacute;rieure, et leur mit les ceps aux pieds.</p>

<p><sup class="versenum">25&nbsp;</sup>Vers le milieu de la nuit, Paul et Silas priaient et chantaient les louanges de Dieu, et les prisonniers les entendaient.</p>

<p><sup class="versenum">26&nbsp;</sup>Tout &agrave; coup il se fit un grand tremblement de terre, en sorte que les fondements de la prison furent &eacute;branl&eacute;s; au m&ecirc;me instant, toutes les portes s&#39;ouvrirent, et les liens de tous les prisonniers furent rompus.</p>

<p><sup class="versenum">27&nbsp;</sup>Le ge&ocirc;lier se r&eacute;veilla, et, lorsqu&#39;il vit les portes de la prison ouvertes, il tira son &eacute;p&eacute;e et allait se tuer, pensant que les prisonniers s&#39;&eacute;taient enfuis.</p>

<p><sup class="versenum">28&nbsp;</sup>Mais Paul cria d&#39;une voix forte: Ne te fais point de mal, nous sommes tous ici.</p>

<p><sup class="versenum">29&nbsp;</sup>Alors le ge&ocirc;lier, ayant demand&eacute; de la lumi&egrave;re, entra pr&eacute;cipitamment, et se jeta tout tremblant aux pieds de Paul et de Silas;</p>

<p><sup class="versenum">30&nbsp;</sup>il les fit sortir, et dit: Seigneurs, que faut-il que je fasse pour &ecirc;tre sauv&eacute;?</p>

<p><sup class="versenum">31&nbsp;</sup>Paul et Silas r&eacute;pondirent: Crois au Seigneur J&eacute;sus, et tu seras sauv&eacute;, toi et ta famille.</p>

<p><sup class="versenum">32&nbsp;</sup>Et ils lui annonc&egrave;rent la parole du Seigneur, ainsi qu&#39;&agrave; tous ceux qui &eacute;taient dans sa maison.</p>

<p><sup class="versenum">33&nbsp;</sup>Il les prit avec lui, &agrave; cette heure m&ecirc;me de la nuit, il lava leurs plaies, et aussit&ocirc;t il fut baptis&eacute;, lui et tous les siens.</p>

<p><sup class="versenum">34&nbsp;</sup>Les ayant conduits dans son logement, il leur servit &agrave; manger, et il se r&eacute;jouit avec toute sa famille de ce qu&#39;il avait cru en Dieu.</p>

<p><sup class="versenum">35&nbsp;</sup>Quand il fit jour, les pr&eacute;teurs envoy&egrave;rent les licteurs pour dire au ge&ocirc;lier: Rel&acirc;che ces hommes.</p>

<p><sup class="versenum">36&nbsp;</sup>Et le ge&ocirc;lier annon&ccedil;a la chose &agrave; Paul: Les pr&eacute;teurs ont envoy&eacute; dire qu&#39;on vous rel&acirc;ch&acirc;t; maintenant donc sortez, et allez en paix.</p>

<p><sup class="versenum">37&nbsp;</sup>Mais Paul dit aux licteurs: Apr&egrave;s nous avoir battus de verges publiquement et sans jugement, nous qui sommes Romains, ils nous ont jet&eacute;s en prison, et maintenant ils nous font sortir secr&egrave;tement! Il n&#39;en sera pas ainsi. Qu&#39;ils viennent eux-m&ecirc;mes nous mettre en libert&eacute;.</p>

<p><sup class="versenum">38&nbsp;</sup>Les licteurs rapport&egrave;rent ces paroles aux pr&eacute;teurs, qui furent effray&eacute;s en apprenant qu&#39;ils &eacute;taient Romains.</p>

<p><sup class="versenum">39&nbsp;</sup>Ils vinrent les apaiser, et ils les mirent en libert&eacute;, en les priant de quitter la ville.</p>

<p><sup class="versenum">40&nbsp;</sup>Quand ils furent sortis de la prison, ils entr&egrave;rent chez Lydie, et, apr&egrave;s avoir vu et exhort&eacute; les fr&egrave;res, ils partirent.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/333.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 16:16-40&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li>L&#39;&eacute;quipe minist&eacute;rielle de Paul, Silas, Timoth&eacute;e et Luc est &agrave; Philippes. Comme il n&#39;y avait pas de synagogue, ils sont all&eacute;s au lieu de pri&egrave;re au bord de la rivi&egrave;re pour chercher d&#39;autres personnes qui avaient un int&eacute;r&ecirc;t pour les questions spirituelles. Une servante poss&eacute;d&eacute;e par un d&eacute;mon a essay&eacute; de s&#39;associer &agrave; l&#39;&eacute;quipe, mais Paul savait par exp&eacute;rience douloureuse le danger qu&rsquo;il y a &agrave; penser qu&#39;il est partisan de fausses pratiques religieuses (<span class="popup-link" @click = "popUp('pop3')"> Actes 14: 8-20</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>A Lystre, se tenait assis un homme impotent des pieds, boiteux de naissance, et qui n&#39;avait jamais march&eacute;.</p>

	<p><sup class="versenum">9&nbsp;</sup>Il &eacute;coutait parler Paul. Et Paul, fixant les regards sur lui et voyant qu&#39;il avait la foi pour &ecirc;tre gu&eacute;ri,</p>

	<p><sup class="versenum">10&nbsp;</sup>dit d&#39;une voix forte: L&egrave;ve-toi droit sur tes pieds. Et il se leva d&#39;un bond et marcha.</p>

	<p><sup class="versenum">11&nbsp;</sup>A la vue de ce que Paul avait fait, la foule &eacute;leva la voix, et dit en langue lycaonienne: Les dieux sous une forme humaine sont descendus vers nous.</p>

	<p><sup class="versenum">12&nbsp;</sup>Ils appelaient Barnabas Jupiter, et Paul Mercure, parce que c&#39;&eacute;tait lui qui portait la parole.</p>

	<p><sup class="versenum">13&nbsp;</sup>Le pr&ecirc;tre de Jupiter, dont le temple &eacute;tait &agrave; l&#39;entr&eacute;e de la ville, amena des taureaux avec des bandelettes vers les portes, et voulait, de m&ecirc;me que la foule, offrir un sacrifice.</p>

	<p><sup class="versenum">14&nbsp;</sup>Les ap&ocirc;tres Barnabas et Paul, ayant appris cela, d&eacute;chir&egrave;rent leurs v&ecirc;tements, et se pr&eacute;cipit&egrave;rent au milieu de la foule,</p>

	<p><sup class="versenum">15&nbsp;</sup>en s&#39;&eacute;criant: O hommes, pourquoi agissez-vous de la sorte? Nous aussi, nous sommes des hommes de la m&ecirc;me nature que vous; et, vous apportant une bonne nouvelle, nous vous exhortons &agrave; renoncer &agrave; ces choses vaines, pour vous tourner vers le Dieu vivant, qui a fait le ciel, la terre, la mer, et tout ce qui s&#39;y trouve.</p>

	<p><sup class="versenum">16&nbsp;</sup>Ce Dieu, dans les &acirc;ges pass&eacute;s, a laiss&eacute; toutes les nations suivre leurs propres voies,</p>

	<p><sup class="versenum">17&nbsp;</sup>quoiqu&#39;il n&#39;ait cess&eacute; de rendre t&eacute;moignage de ce qu&#39;il est, en faisant du bien, en vous dispensant du ciel les pluies et les saisons fertiles, en vous donnant la nourriture avec abondance et en remplissant vos coeurs de joie.</p>

	<p><sup class="versenum">18&nbsp;</sup>A peine purent-ils, par ces paroles, emp&ecirc;cher la foule de leur offrir un sacrifice.</p>

	<p><sup class="versenum">19&nbsp;</sup>Alors survinrent d&#39;Antioche et d&#39;Icone des Juifs qui gagn&egrave;rent la foule, et qui, apr&egrave;s avoir lapid&eacute; Paul, le tra&icirc;n&egrave;rent hors de la ville, pensant qu&#39;il &eacute;tait mort.</p>

	<p><sup class="versenum">20&nbsp;</sup>Mais, les disciples l&#39;ayant entour&eacute;, il se leva, et entra dans la ville. Le lendemain, il partit pour Derbe avec Barnabas.</p>
	<!-- end bible --></div>
	La puissance de J&eacute;sus a vaincu l&#39;esprit d&eacute;moniaque et a lib&eacute;r&eacute; la fille. Parce que ses ma&icirc;tres ne pouvaient plus l&#39;utiliser pour gagner de l&#39;argent, ils ont faussement accus&eacute; Paul et Silas d&#39;introduire des coutumes ill&eacute;gales ; ce qui a conduit &agrave; leur arrestation. M&ecirc;me en ces circonstances difficiles, Paul et Silas ont mis leur confiance dans le Seigneur en l&#39;adorant en prison. Dans ce cas de pers&eacute;cution, le Seigneur a fait un miracle. Comme l&rsquo;&oelig;uvre miraculeuse du Seigneur, le ge&ocirc;lier s&rsquo;est r&eacute;v&eacute;l&eacute; &ecirc;tre une personne de paix pr&eacute;par&eacute;e par Dieu. Le ge&ocirc;lier et toute sa maison ont cru en J&eacute;sus. Avant le d&eacute;part de l&#39;&eacute;quipe, ils ont encourag&eacute; les croyants de la nouvelle &eacute;glise qui se r&eacute;unissait dans la maison de Lydie.</li>
</ul>

<p>&nbsp;</p>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<p><span class="tlid-translation translation" lang="fr"><span title="">Pratiquez les comp&eacute;tences n&eacute;cessaires ou les sujets pr&eacute;c&eacute;dents pour vous pr&eacute;parer &agrave; servir les autres:</span></span></p>

<ul>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Pri&egrave;re, soins, partage</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Gospel</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">&Eacute;tudes bibliques fondamentales.</span></span></li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
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

			<td class="social" @click="share('lesson', 'Des personnes de paix dans des lieux improbables: ', '/content/M2/fra/multiply3/multiply333.html')">
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