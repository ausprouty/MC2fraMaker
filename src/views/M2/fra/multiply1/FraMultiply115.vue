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
                        <div class="chapter_number ltr"><h1>15.</h1></div>
                        <div class="chapter_title ltr"><h1>Donner avec Objectif</h1></div>
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
	<li>Exemple: <span class="popup-link" @click = "popUp('pop1')"> H&eacute;breux 4:14-16</span>&nbsp;et ex&eacute;cutez des chants.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Ainsi, puisque nous avons un grand souverain sacrificateur qui a travers&eacute; les cieux, J&eacute;sus, le Fils de Dieu, demeurons fermes dans la foi que nous professons.</p>

	<p><sup class="versenum">15&nbsp;</sup>Car nous n&#39;avons pas un souverain sacrificateur qui ne puisse compatir &agrave; nos faiblesses; au contraire, il a &eacute;t&eacute; tent&eacute; comme nous en toutes choses, sans commettre de p&eacute;ch&eacute;.</p>

	<p><sup class="versenum">16&nbsp;</sup>Approchons-nous donc avec assurance du tr&ocirc;ne de la gr&acirc;ce afin d&#39;obtenir mis&eacute;ricorde et de trouver gr&acirc;ce, pour &ecirc;tre secourus dans nos besoins.</p>
	<!-- end bible --></div>
	</li>
	<li>(facultatif) Utilisez une d&eacute;claration de foi au sujet de J&eacute;sus comme <span class="popup-link" @click = "popUp('pop2')"> Philippiens 2:11b</span>
	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	+ <span class="popup-link" @click = "popUp('pop3')"> 1 Timoth&eacute;e 2:4-6a</span>

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
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

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<p>Exemple: Un jour, J&eacute;sus envoya ses disciples pour pr&ecirc;cher aux habitants des villages voisins. A leur retour ils &eacute;taient si contents de ce que Dieu a fait &agrave; travers eux, &laquo; Seigneur, m&ecirc;me les d&eacute;mons nous ob&eacute;issent quand nous utilisons ton nom!&raquo; Apr&egrave;s s&rsquo;&ecirc;tre r&eacute;jouis avec eux, J&eacute;sus leur donna cette perspective &laquo; Cependant, ne vous r&eacute;jouissez pas de ce que les esprits vous sont soumis; mais r&eacute;jouissez-vous de ce que vos nom sont &eacute;crits dans les cieux. &raquo; (<span class="popup-link" @click = "popUp('pop6')"> Luc 10:17-20</span>)&nbsp;</p>

<div class="popup invisible" id="pop6"><!-- begin bible -->
<p><sup class="versenum">17&nbsp;</sup>Les soixante-dix revinrent avec joie, disant: Seigneur, les d&eacute;mons m&ecirc;mes nous sont soumis en ton nom.</p>

<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus leur dit: Je voyais Satan tomber du ciel comme un &eacute;clair.</p>

<p><sup class="versenum">19&nbsp;</sup>Voici, je vous ai donn&eacute; le pouvoir de marcher sur les serpents et les scorpions, et sur toute la puissance de l&#39;ennemi; et rien ne pourra vous nuire.</p>

<p><sup class="versenum">20&nbsp;</sup>Cependant, ne vous r&eacute;jouissez pas de ce que les esprits vous sont soumis; mais r&eacute;jouissez-vous de ce que vos noms sont &eacute;crits dans les cieux.</p>
<!-- end bible --></div>
J&eacute;sus nous rappelle que notre joie ne se trouve pas dans les r&eacute;sultats mais plut&ocirc;t en ce que nous Le connaissons!

<p>&nbsp;</p>

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

<p>Les chr&eacute;tiens de l&rsquo;&eacute;glise primitive s&rsquo;&eacute;taient engag&eacute;s les uns envers les autres. Ils se r&eacute;unissaient r&eacute;guli&egrave;rement et plusieurs nouvelles personnes venaient &agrave; Christ. Apr&egrave;s un temps de pers&eacute;cution, ils pri&egrave;rent pour avoir de la hardiesse et le Seigneur les a aid&eacute;s &agrave; parler de l&rsquo;&eacute;vangile avec audace. Cette histoire au sujet des croyants de J&eacute;rusalem montre leur engagement les uns envers les autres.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Actes 4:32-37&nbsp;deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 4:32-37</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">32&nbsp;</sup>La multitude de ceux qui avaient cru n&#39;&eacute;tait qu&#39;un coeur et qu&#39;une &acirc;me. Nul ne disait que ses biens lui appartinssent en propre, mais tout &eacute;tait commun entre eux.</p>

<p><sup class="versenum">33&nbsp;</sup>Les ap&ocirc;tres rendaient avec beaucoup de force t&eacute;moignage de la r&eacute;surrection du Seigneur J&eacute;sus. Et une grande gr&acirc;ce reposait sur eux tous.</p>

<p><sup class="versenum">34&nbsp;</sup>Car il n&#39;y avait parmi eux aucun indigent: tous ceux qui poss&eacute;daient des champs ou des maisons les vendaient, apportaient le prix de ce qu&#39;ils avaient vendu,</p>

<p><sup class="versenum">35&nbsp;</sup>et le d&eacute;posaient aux pieds des ap&ocirc;tres; et l&#39;on faisait des distributions &agrave; chacun selon qu&#39;il en avait besoin.</p>

<p><sup class="versenum">36&nbsp;</sup>Joseph, surnomm&eacute; par les ap&ocirc;tres Barnabas, ce qui signifie fils d&#39;exhortation, L&eacute;vite, originaire de Chypre,</p>

<p><sup class="versenum">37&nbsp;</sup>vendit un champ qu&#39;il poss&eacute;dait, apporta l&#39;argent, et le d&eacute;posa aux pieds des ap&ocirc;tres.</p>

<p>&nbsp;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/115.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 4:32-37&nbsp; </button>
    <div class="collapsed"></div>




<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (ce passage)?</li>
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
	<li>Relisez l&rsquo;histoire. Amenez quelqu&rsquo;un &agrave; raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<ul>
	<li class="nobreak-final-final">M&ecirc;me depuis le commencement de l&rsquo;Eglise, les croyants prenaient soin des besoins les uns des autres en donnant. Nous apprenons de cette histoire que nous devons donner volontairement, sans contrainte. Ceci est clairement dit dans <span class="popup-link" @click = "popUp('pop4')"> 2 Corinthiens 9:7</span>.&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>Que chacun donne comme il l&#39;a r&eacute;solu en son coeur, sans tristesse ni contrainte; car Dieu aime celui qui donne avec joie.</p>
	<!-- end bible --></div>
	Lisez <span class="popup-link" @click = "popUp('pop5')"> Actes 11:27-29</span>.&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">27&nbsp;</sup>En ce temps-l&agrave;, des proph&egrave;tes descendirent de J&eacute;rusalem &agrave; Antioche.</p>

	<p><sup class="versenum">28&nbsp;</sup>L&#39;un deux, nomm&eacute; Agabus, se leva, et annon&ccedil;a par l&#39;Esprit qu&#39;il y aurait une grande famine sur toute la terre. Elle arriva, en effet, sous Claude.</p>

	<p><sup class="versenum">29&nbsp;</sup>Les disciples r&eacute;solurent d&#39;envoyer, chacun selon ses moyens, un secours aux fr&egrave;res qui habitaient la Jud&eacute;e.</p>
	<!-- end bible --></div>
	L&rsquo;Eglise primitive a aussi donn&eacute; aux croyants d&rsquo;autres &eacute;glises. Cela montre que nos dons peuvent &ecirc;tre utilis&eacute;s en dehors de notre propre &eacute;glise. Lisez <span class="popup-link" @click = "popUp('pop7')"> Luc 8:1-3</span>.&nbsp;

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Ensuite, J&eacute;sus allait de ville en ville et de village en village, pr&ecirc;chant et annon&ccedil;ant la bonne nouvelle du royaume de Dieu.</p>

	<p><sup class="versenum">2&nbsp;</sup>Les douze &eacute;taient avec de lui et quelques femmes qui avaient &eacute;t&eacute; gu&eacute;ries d&#39;esprits malins et de maladies: Marie, dite de Magdala, de laquelle &eacute;taient sortis sept d&eacute;mons,</p>

	<p><sup class="versenum">3&nbsp;</sup>Jeanne, femme de Chuza, intendant d&#39;H&eacute;rode, Susanne, et plusieurs autres, qui l&#39;assistaient de leurs biens.</p>
	<!-- end bible --></div>
	Cette histoire nous montre aussi que les dons sont aussi utilis&eacute;s pour amener l&rsquo;&eacute;vangile &agrave; d&rsquo;autres endroits et propager le message de Dieu. Dans <span class="popup-link" @click = "popUp('pop8')"> 1 Corinthiens 16:2</span>.

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Que chacun de vous, le premier jour de la semaine, mette &agrave; part chez lui ce qu&#39;il pourra, selon sa prosp&eacute;rit&eacute;, afin qu&#39;on n&#39;attende pas mon arriv&eacute;e pour recueillir les dons.</p>
	<!-- end bible --></div>
	&nbsp;Paul encourage les gens &agrave; pratiquer la lib&eacute;ralit&eacute; chaque semaine afin que les dons puissent &ecirc;tre utilis&eacute;s pour les objectifs pr&eacute;cit&eacute;s.</li>
</ul>

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
	<li>Discutez de comment la lib&eacute;ralit&eacute; va &ecirc;tre g&eacute;r&eacute;e.</li>
	<li>Identifiez des besoins o&ugrave; vos dons peuvent &ecirc;tre utilis&eacute;s.</li>
	<li>Rappelez-vous du sacrifice &agrave; travers la Sainte C&egrave;ne si appropri&eacute;.</li>
	<li>Pratiquez n&#39;importe quelle comp&eacute;tence ou sujet des le&ccedil;ons pr&eacute;c&eacute;dentes pour aider &agrave; pr&eacute;parer &agrave; prendre soin des autres.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>Ecrivez les promesses &laquo; Je le ferai d&rsquo;ici quand&raquo;.et parlez-en &agrave; votre groupe</li>
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

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</p>
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

			<td class="social" @click="share('lesson', 'Donner avec Objectif: ', '/content/M2/fra/multiply1/multiply115.html')">
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