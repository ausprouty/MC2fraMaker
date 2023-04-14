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
                        <div class="chapter_number ltr"><h1>2.</h1></div>
                        <div class="chapter_title ltr"><h1>Matthias choisi pour remplacer Judas</h1></div>
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
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>).

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
	<li>Lisez ou observez Actes 1:12-26&nbsp;deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 1:12-26</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>Alors ils retourn&egrave;rent &agrave; J&eacute;rusalem, de la montagne appel&eacute;e des oliviers, qui est pr&egrave;s de J&eacute;rusalem, &agrave; la distance d&#39;un chemin de sabbat.</p>

<p><sup class="versenum">13&nbsp;</sup>Quand ils furent arriv&eacute;s, ils mont&egrave;rent dans la chambre haute o&ugrave; ils se tenaient d&#39;ordinaire; c&#39;&eacute;taient Pierre, Jean, Jacques, Andr&eacute;, Philippe, Thomas, Barth&eacute;lemy, Matthieu, Jacques, fils d&#39;Alph&eacute;e, Simon le Z&eacute;lote, et Jude, fils de Jacques.</p>

<p><sup class="versenum">14&nbsp;</sup>Tous d&#39;un commun accord pers&eacute;v&eacute;raient dans la pri&egrave;re, avec les femmes, et Marie, m&egrave;re de J&eacute;sus, et avec les fr&egrave;res de J&eacute;sus.</p>

<p><sup class="versenum">15&nbsp;</sup>En ces jours-l&agrave;, Pierre se leva au milieu des fr&egrave;res, le nombre des personnes r&eacute;unies &eacute;tant d&#39;environ cent vingt. Et il dit:</p>

<p><sup class="versenum">16&nbsp;</sup>Hommes fr&egrave;res, il fallait que s&#39;accompl&icirc;t ce que le Saint Esprit, dans l&#39;&Eacute;criture, a annonc&eacute; d&#39;avance, par la bouche de David, au sujet de Judas, qui a &eacute;t&eacute; le guide de ceux qui ont saisi J&eacute;sus.</p>

<p><sup class="versenum">17&nbsp;</sup>Il &eacute;tait compt&eacute; parmi nous, et il avait part au m&ecirc;me minist&egrave;re.</p>

<p><sup class="versenum">18&nbsp;</sup>Cet homme, ayant acquis un champ avec le salaire du crime, est tomb&eacute;, s&#39;est rompu par le milieu du corps, et toutes ses entrailles se sont r&eacute;pandues.</p>

<p><sup class="versenum">19&nbsp;</sup>La chose a &eacute;t&eacute; si connue de tous les habitants de J&eacute;rusalem que ce champ a &eacute;t&eacute; appel&eacute; dans leur langue Hakeldama, c&#39;est-&agrave;-dire, champ du sang.</p>

<p><sup class="versenum">20&nbsp;</sup>Or, il est &eacute;crit dans le livre des Psaumes: Que sa demeure devienne d&eacute;serte, Et que personne ne l&#39;habite! Et: Qu&#39;un autre prenne sa charge!</p>

<p><sup class="versenum">21&nbsp;</sup>Il faut donc que, parmi ceux qui nous ont accompagn&eacute;s tout le temps que le Seigneur J&eacute;sus a v&eacute;cu avec nous,</p>

<p><sup class="versenum">22&nbsp;</sup>depuis le bapt&ecirc;me de Jean jusqu&#39;au jour o&ugrave; il a &eacute;t&eacute; enlev&eacute; du milieu de nous, il y en ait un qui nous soit associ&eacute; comme t&eacute;moin de sa r&eacute;surrection.</p>

<p><sup class="versenum">23&nbsp;</sup>Ils en pr&eacute;sent&egrave;rent deux: Joseph appel&eacute; Barsabbas, surnomm&eacute; Justus, et Matthias.</p>

<p><sup class="versenum">24&nbsp;</sup>Puis ils firent cette pri&egrave;re: Seigneur, toi qui connais les coeurs de tous, d&eacute;signe lequel de ces deux tu as choisi,</p>

<p><sup class="versenum">25&nbsp;</sup>afin qu&#39;il ait part &agrave; ce minist&egrave;re et &agrave; cet apostolat, que Judas a abandonn&eacute; pour aller en son lieu.</p>

<p><sup class="versenum">26&nbsp;</sup>Ils tir&egrave;rent au sort, et le sort tomba sur Matthias, qui fut associ&eacute; aux onze ap&ocirc;tres.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/302.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 1:12-26&nbsp; </button>
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

<p>Il restait seulement 120 disciples &agrave; J&eacute;rusalem en ce moment. La m&egrave;re, les fr&egrave;res et les s&oelig;urs de J&eacute;sus &eacute;taient &agrave; pr&eacute;sent compt&eacute;s parmi les croyants. Cette histoire montre que, bien qu&rsquo;ils ne soient pas mentionn&eacute;s dans les &Eacute;vangiles, il y avait plusieurs d&rsquo;autres qui suivaient J&eacute;sus depuis le moment o&ugrave; Il fut baptis&eacute; jusqu&rsquo;au moment o&ugrave; Il retourna au ciel. J&eacute;sus a choisi les douze premiers ap&ocirc;tres parmi de nombreux autres candidats. Les onze restants ont d&eacute;cid&eacute; que le principal crit&egrave;re de s&eacute;lection d&rsquo;un rempla&ccedil;ant &eacute;tait le temps pass&eacute; &agrave; &ecirc;tre t&eacute;moin de la vie et du minist&egrave;re de J&eacute;sus. C&rsquo;est la derni&egrave;re fois que nous voyons qu&rsquo;ils se sont servis d&rsquo;un tirage au sort &agrave; la mani&egrave;re de l&rsquo;Ancien Testament pour prendre des d&eacute;cisions. J&eacute;sus n&rsquo;a jamais utilis&eacute; le tirage au sort pour discerner la volont&eacute; du P&egrave;re parce qu&rsquo;il a &eacute;cout&eacute; et ob&eacute;i &agrave; l&rsquo;Esprit. Apr&egrave;s la venue de l&#39;Esprit, discerner la volont&eacute; de Dieu se fait en se soumettant et en restant en phase avec l&#39;Esprit.</p>

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

			<td class="social" @click="share('lesson', 'Matthias choisi pour remplacer Judas: ', '/content/M2/fra/multiply3/multiply302.html')">
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