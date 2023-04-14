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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply2-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>18.</h1></div>
                        <div class="chapter_title ltr"><h1>Première Expédition de la Pêche d’hommes</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

</div>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Marc 1:21-28 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Marc 1:21-28</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">21&nbsp;</sup>Ils se rendirent &agrave; Caperna&uuml;m. Et, le jour du sabbat, J&eacute;sus entra d&#39;abord dans la synagogue, et il enseigna.</p>

<p><sup class="versenum">22&nbsp;</sup>Ils &eacute;taient frapp&eacute;s de sa doctrine; car il enseignait comme ayant autorit&eacute;, et non pas comme les scribes.</p>

<p><sup class="versenum">23&nbsp;</sup>Il se trouva dans leur synagogue un homme qui avait un esprit impur, et qui s&#39;&eacute;cria:</p>

<p><sup class="versenum">24&nbsp;</sup>Qu&#39;y a-t-il entre nous et toi, J&eacute;sus de Nazareth? Tu es venu pour nous perdre. Je sais qui tu es: le Saint de Dieu.</p>

<p><sup class="versenum">25&nbsp;</sup>J&eacute;sus le mena&ccedil;a, disant: Tais-toi, et sors de cet homme.</p>

<p><sup class="versenum">26&nbsp;</sup>Et l&#39;esprit impur sortit de cet homme, en l&#39;agitant avec violence, et en poussant un grand cri.</p>

<p><sup class="versenum">27&nbsp;</sup>Tous furent saisis de stup&eacute;faction, de sorte qu&#39;il se demandaient les uns aux autres: Qu&#39;est-ce que ceci? Une nouvelle doctrine! Il commande avec autorit&eacute; m&ecirc;me aux esprits impurs, et ils lui ob&eacute;issent!</p>

<p><sup class="versenum">28&nbsp;</sup>Et sa renomm&eacute;e se r&eacute;pandit aussit&ocirc;t dans tous les lieux environnants de la Galil&eacute;e.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/218.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 1:21-28&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<p>Etudiez chaque passage en utilisant les questions de discussion suivantes:</p>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
</ul>

<p>Questions suppl&eacute;mentaires que vous pouvez poser:</p>

<ul>
	<li>Qu&rsquo;est-ce que ses disciples apprennent?</li>
	<li>Qu&rsquo;est-ce que J&eacute;sus est en train de nous montrer au sujet de sa vie et de son minist&egrave;re (ou leadership) ?</li>
	<li>Qu&rsquo;est ce que J&eacute;sus est en train de montrer au sujet du leadership empreint de pi&eacute;t&eacute; ?</li>
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

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>J&eacute;sus commence le premier des six campagnes d&rsquo;&eacute;vang&eacute;lisation afin de former Sa jeune &eacute;quipe du minist&egrave;re pour atteindre les foules avec la Bonne Nouvelle qu&#39;Il est le Messie. Le premier voyage est dans leur lieu de culte, la synagogue locale. L&agrave;, ils trouvent un groupe de religieux perdu. J&eacute;sus utilise les cinq premiers livres de la Bible pour partager avec eux ce qu&#39;Il est. Il combine cela avec le message qu&#39;il est temps de se repentir parce que le Royaume de Dieu est ici. La foule a reconnu qu&#39;Il &eacute;tait diff&eacute;rent et a &eacute;t&eacute; &eacute;tonn&eacute; que J&eacute;sus ait eu le contr&ocirc;le sur les mauvais esprits. Il semble que c&#39;est la premi&egrave;re fois que J&eacute;sus a chass&eacute; un d&eacute;mon et que les nouvelles de cet &eacute;v&eacute;nement se r&eacute;pandent rapidement. Le d&eacute;mon a d&eacute;montr&eacute; qu&#39;il savait exactement qui &eacute;tait J&eacute;sus, &laquo; le Saint de Dieu. &raquo;</p>

<p>Etude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 4:31-37</span>.</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">31&nbsp;</sup>Il descendit &agrave; Caperna&uuml;m, ville de la Galil&eacute;e; et il enseignait, le jour du sabbat.</p>

<p><sup class="versenum">32&nbsp;</sup>On &eacute;tait frapp&eacute; de sa doctrine; car il parlait avec autorit&eacute;.</p>

<p><sup class="versenum">33&nbsp;</sup>Il se trouva dans la synagogue un homme qui avait un esprit de d&eacute;mon impur, et qui s&#39;&eacute;cria d&#39;une voix forte:</p>

<p><sup class="versenum">34&nbsp;</sup>Ah! qu&#39;y a-t-il entre nous et toi, J&eacute;sus de Nazareth? Tu es venu pour nous perdre. Je sais qui tu es: le Saint de Dieu.</p>

<p><sup class="versenum">35&nbsp;</sup>J&eacute;sus le mena&ccedil;a, disant: Tais-toi, et sors de cet homme. Et le d&eacute;mon le jeta au milieu de l&#39;assembl&eacute;e, et sortit de lui, sans lui faire aucun mal.</p>

<p><sup class="versenum">36&nbsp;</sup>Tous furent saisis de stupeur, et ils se disaient les uns aux autres: Quelle est cette parole? il commande avec autorit&eacute; et puissance aux esprits impurs, et ils sortent!</p>

<p><sup class="versenum">37&nbsp;</sup>Et sa renomm&eacute;e se r&eacute;pandit dans tous les lieux d&#39;alentour.</p>
<!-- end bible --></div>

<p>&nbsp;</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
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

<h2>Aller en Mission</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez les promesses &laquo; je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
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

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<p>&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Première Expédition de la Pêche d’hommes: ', '/content/M2/fra/multiply2/multiply218.html')">
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