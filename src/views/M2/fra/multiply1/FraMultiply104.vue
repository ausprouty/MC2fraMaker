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
                        <div class="chapter_number ltr"><h1>4.</h1></div>
                        <div class="chapter_title ltr"><h1>S’identifier à Jésus avec Hardiesse</h1></div>
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

<p>Lisez un passage biblique pour commencer &agrave; poser les fondements de l&rsquo;adoration et de la louange.</p>

<p>Exemple: <span class="popup-link" @click = "popUp('pop1')"> Psaumes 29:2</span></p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">2&nbsp;</sup>Rendez &agrave; l&#39;&Eacute;ternel gloire pour son nom! Prosternez-vous devant l&#39;&Eacute;ternel avec des ornements sacr&eacute;s!</p>
<!-- end bible --></div>
&laquo; Rendez &agrave; l&rsquo;Eternel gloire pour son nom! Prosternez-vous devant l&rsquo;&Eacute;ternel avec des ornements sacr&eacute;s! &raquo; Marquons une pause et rendons gloire &agrave; l&rsquo;&Eacute;ternel en Le louant.

<p>&nbsp;</p>

</div>

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

<ul>
	<li class="nobreak-final-final">Exemple: Non seulement le Seigneur nous aime, mais il a aussi une vision pour nos vies. Qu&rsquo;est-ce que la vision? C&rsquo;est d&rsquo;&ecirc;tre comme Christ. <span class="popup-link" @click = "popUp('pop2')"> Romains 8:29</span>

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">29&nbsp;</sup>Car ceux qu&#39;il a connus d&#39;avance, il les a aussi pr&eacute;destin&eacute;s &agrave; &ecirc;tre semblables &agrave; l&#39;image de son Fils, afin que son Fils f&ucirc;t le premier-n&eacute; entre plusieurs fr&egrave;res.</p>
	<!-- end bible --></div>
	d&eacute;clare que Son plan est que nous soyons &agrave; l&rsquo;image de son Fils pour exp&eacute;rimenter et refl&eacute;ter le P&egrave;re comme le Fils l&rsquo;a fait, et la bonne nouvelle est que cette &oelig;uvre qui consiste &agrave; refl&eacute;ter Christ est l&rsquo;&oelig;uvre de Dieu. <span class="popup-link" @click = "popUp('pop3')"> Philippiens 1:6</span>

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">6&nbsp;</sup>Je suis persuad&eacute; que celui qui a commenc&eacute; en vous cette bonne oeuvre la rendra parfaite pour le jour de J&eacute;sus Christ.</p>
	<!-- end bible --></div>
	nous fait la promesse que &laquo; Celui qui a commenc&eacute; en vous cette bonne &oelig;uvre la rendra parfaite pour le jour de J&eacute;sus Christ &raquo;. Soyez encourag&eacute;s du fait que Dieu fera son &oelig;uvre dans votre vie pour qu&rsquo;elle refl&egrave;te celle de Christ.</li>
</ul>

</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ Contexte</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Un fid&egrave;le de J&eacute;sus appel&eacute; Philippe annon&ccedil;ait la bonne nouvelle &agrave; certaines personnes dans une localit&eacute; d&rsquo;Isra&euml;l appel&eacute; Samarie. Le Seigneur a interrompu son minist&egrave;re et lui demanda de se rendre au sud sur la route qui m&egrave;ne &agrave; l&rsquo;Egypte. En chemin, il trouva un leader africain (eunuque) qui se rendait sur sa terre natale. Cette histoire nous relate ce qui s&rsquo;est pass&eacute;.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Actes 8:34-40 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 8:34-40</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">34&nbsp;</sup>L&#39;eunuque dit &agrave; Philippe: Je te prie, de qui le proph&egrave;te parle-t-il ainsi? Est-ce de lui-m&ecirc;me, ou de quelque autre?</p>

<p><sup class="versenum">35&nbsp;</sup>Alors Philippe, ouvrant la bouche et commen&ccedil;ant par ce passage, lui annon&ccedil;a la bonne nouvelle de J&eacute;sus.</p>

<p><sup class="versenum">36&nbsp;</sup>Comme ils continuaient leur chemin, ils rencontr&egrave;rent de l&#39;eau. Et l&#39;eunuque dit: Voici de l&#39;eau; qu&#39;est-ce qui emp&ecirc;che que je ne sois baptis&eacute;?</p>

<p><sup class="versenum">37&nbsp;</sup>Philippe dit: Si tu crois de tout ton coeur, cela est possible. L&#39;eunuque r&eacute;pondit: Je crois que J&eacute;sus Christ est le Fils de Dieu.</p>

<p><sup class="versenum">38&nbsp;</sup>Il fit arr&ecirc;ter le char; Philippe et l&#39;eunuque descendirent tous deux dans l&#39;eau, et Philippe baptisa l&#39;eunuque.</p>

<p><sup class="versenum">39&nbsp;</sup>Quand ils furent sortis de l&#39;eau, l&#39;Esprit du Seigneur enleva Philippe, et l&#39;eunuque ne le vit plus. Tandis que, joyeux, il poursuivait sa route,</p>

<p><sup class="versenum">40&nbsp;</sup>Philippe se trouva dans Azot, d&#39;o&ugrave; il alla jusqu&#39;&agrave; C&eacute;sar&eacute;e, en &eacute;vang&eacute;lisant toutes les villes par lesquelles il passait.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/104.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 8:34-40&nbsp; </button>
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

<p>Lisez <span class="popup-link" @click = "popUp('pop4')"> Matthieu 3:13-17</span>.</p>

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">13&nbsp;</sup>Alors J&eacute;sus vint de la Galil&eacute;e au Jourdain vers Jean, pour &ecirc;tre baptis&eacute; par lui.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais Jean s&#39;y opposait, en disant: C&#39;est moi qui ai besoin d&#39;&ecirc;tre baptis&eacute; par toi, et tu viens &agrave; moi!</p>

<p><sup class="versenum">15&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Laisse faire maintenant, car il est convenable que nous accomplissions ainsi tout ce qui est juste. Et Jean ne lui r&eacute;sista plus.</p>

<p><sup class="versenum">16&nbsp;</sup>D&egrave;s que J&eacute;sus eut &eacute;t&eacute; baptis&eacute;, il sortit de l&#39;eau. Et voici, les cieux s&#39;ouvrirent, et il vit l&#39;Esprit de Dieu descendre comme une colombe et venir sur lui.</p>

<p><sup class="versenum">17&nbsp;</sup>Et voici, une voix fit entendre des cieux ces paroles: Celui-ci est mon Fils bien-aim&eacute;, en qui j&#39;ai mis toute mon affection.</p>
<!-- end bible --></div>
&nbsp;J&eacute;sus Lui-m&ecirc;me fut baptis&eacute; et donna ainsi l&rsquo;exemple &agrave; ses disciples. Depuis le temps de Christ, quiconque d&eacute;cide de le suivre prend cet engagement. Notre volont&eacute; d&rsquo;&ecirc;tre baptis&eacute; d&eacute;montre aux autres qu&rsquo;un r&eacute;el changement s&rsquo;est op&eacute;r&eacute; dans notre vie. Cela symbolise que nous nous identifions avec hardiesse &agrave; la mort et &agrave; la r&eacute;surrection de J&eacute;sus (<span class="popup-link" @click = "popUp('pop5')"> Romains 6:4-5</span>).

<div class="popup invisible" id="pop5"><!-- begin bible -->
<p><sup class="versenum">4&nbsp;</sup>Nous avons donc &eacute;t&eacute; ensevelis avec lui par le bapt&ecirc;me en sa mort, afin que, comme Christ est ressuscit&eacute; des morts par la gloire du P&egrave;re, de m&ecirc;me nous aussi nous marchions en nouveaut&eacute; de vie.</p>

<p><sup class="versenum">5&nbsp;</sup>En effet, si nous sommes devenus une m&ecirc;me plante avec lui par la conformit&eacute; &agrave; sa mort, nous le serons aussi par la conformit&eacute; &agrave; sa r&eacute;surrection,</p>
<!-- end bible --></div>
&nbsp;

</div>
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
	<li>Appliquez-vous &agrave; engager une conversation, &agrave; partager la bonne nouvelle ou &agrave; d&eacute;marrer le processus de suivi.</li>
	<li>Rappelez-leur ce qu&rsquo;il faut faire lorsque quelqu&rsquo;un dit OUI &agrave; l&rsquo;&eacute;vangile.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre liste de r&eacute;seau, &agrave; qui vous raconterez l&rsquo;histoire ou annoncerez la bonne nouvelle cette semaine</li>
	<li>Si quelqu&rsquo;un veut se faire baptiser, fixez un temps pour le faire.</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

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

			<td class="social" @click="share('lesson', 'S’identifier à Jésus avec Hardiesse: ', '/content/M2/fra/multiply1/multiply104.html')">
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