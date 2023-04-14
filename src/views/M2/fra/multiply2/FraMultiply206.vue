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
                        <div class="chapter_number ltr"><h1>6.</h1></div>
                        <div class="chapter_title ltr"><h1>L’identité de Jésus révélée</h1></div>
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
<div class="lesson-subtitle">Chercher</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Matthieu 3:13-17 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 3:13-17</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">13&nbsp;</sup>Alors J&eacute;sus vint de la Galil&eacute;e au Jourdain vers Jean, pour &ecirc;tre baptis&eacute; par lui.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais Jean s&#39;y opposait, en disant: C&#39;est moi qui ai besoin d&#39;&ecirc;tre baptis&eacute; par toi, et tu viens &agrave; moi!</p>

<p><sup class="versenum">15&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Laisse faire maintenant, car il est convenable que nous accomplissions ainsi tout ce qui est juste. Et Jean ne lui r&eacute;sista plus.</p>

<p><sup class="versenum">16&nbsp;</sup>D&egrave;s que J&eacute;sus eut &eacute;t&eacute; baptis&eacute;, il sortit de l&#39;eau. Et voici, les cieux s&#39;ouvrirent, et il vit l&#39;Esprit de Dieu descendre comme une colombe et venir sur lui.</p>

<p><sup class="versenum">17&nbsp;</sup>Et voici, une voix fit entendre des cieux ces paroles: Celui-ci est mon Fils bien-aim&eacute;, en qui j&#39;ai mis toute mon affection.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/206.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 3:13-17&nbsp; </button>
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

<ul>
	<li class="nobreak-final-final">Lisez <span class="popup-link" @click = "popUp('pop1')"> Luc 3:23</span>.&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus avait environ trente ans lorsqu&#39;il commen&ccedil;a son minist&egrave;re, &eacute;tant, comme on le croyait, fils de Joseph, fils d&#39;H&eacute;li,</p>
	<!-- end bible --></div>
	&nbsp;J&eacute;sus quitta sa maison en Galil&eacute;e. Il pourrait ne pas avoir &eacute;t&eacute; s&ucirc;r de ses prochaines &eacute;tapes mais le P&egrave;re le conduit &agrave; &ecirc;tre baptis&eacute; par Jean. Le Bapt&ecirc;me &eacute;tait utilis&eacute; pour identifier un messager et son message. Luc 3 :23 dit qu&rsquo;Il a commenc&eacute; son minist&egrave;re lorsqu&rsquo;il avait environ 30 ans</li>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie : <span class="popup-link" @click = "popUp('pop2')"> Luc 3:21-23</span>; &nbsp;
	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">21&nbsp;</sup>Tout le peuple se faisant baptiser, J&eacute;sus fut aussi baptis&eacute;; et, pendant qu&#39;il priait, le ciel s&#39;ouvrit,</p>

	<p><sup class="versenum">22&nbsp;</sup>et le Saint Esprit descendit sur lui sous une forme corporelle, comme une colombe. Et une voix fit entendre du ciel ces paroles: Tu es mon Fils bien-aim&eacute;; en toi j&#39;ai mis toute mon affection.</p>

	<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus avait environ trente ans lorsqu&#39;il commen&ccedil;a son minist&egrave;re, &eacute;tant, comme on le croyait, fils de Joseph, fils d&#39;H&eacute;li,</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Marc 1: 9-11</span>.

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>En ce temps-l&agrave;, J&eacute;sus vint de Nazareth en Galil&eacute;e, et il fut baptis&eacute; par Jean dans le Jourdain.</p>

	<p><sup class="versenum">10&nbsp;</sup>Au moment o&ugrave; il sortait de l&#39;eau, il vit les cieux s&#39;ouvrir, et l&#39;Esprit descendre sur lui comme une colombe.</p>

	<p><sup class="versenum">11&nbsp;</sup>Et une voix fit entendre des cieux ces paroles: Tu es mon Fils bien-aim&eacute;, en toi j&#39;ai mis toute mon affection.</p>
	<!-- end bible --></div>
	</li>
</ul>

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

			<td class="social" @click="share('lesson', 'L’identité de Jésus révélée: ', '/content/M2/fra/multiply2/multiply206.html')">
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