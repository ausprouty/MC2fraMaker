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
                        <div class="chapter_number ltr"><h1>16.</h1></div>
                        <div class="chapter_title ltr"><h1>Coût du Discipôlat</h1></div>
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
	<li>Lisez <span class="popup-link" @click = "popUp('pop1')"> H&eacute;breux 13:14-15</span>&nbsp;et ex&eacute;cutez des cantiques.

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Car nous n&#39;avons point ici-bas de cit&eacute; permanente, mais nous cherchons celle qui est &agrave; venir.</p>

	<p><sup class="versenum">15&nbsp;</sup>Par lui, offrons sans cesse &agrave; Dieu un sacrifice de louange, c&#39;est-a-dire le fruit de l&egrave;vres qui confessent son nom.</p>
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

<p>Exemple: Le c&oelig;ur de Dieu est pour tous les perdus. Pourtant, tant d&#39;endroits autour de nous sont sans disciples de J&eacute;sus qui puissent &ecirc;tre une lumi&egrave;re pour la communaut&eacute; et t&eacute;moigner de l&#39;amour de Dieu aux gens en ces lieux. En tant que disciples de J&eacute;sus, nous sommes appel&eacute;s par Dieu &agrave; aligner nos c&oelig;urs &agrave; Son c&oelig;ur pour TOUS les perdus. Nous devons poursuivre une grande vision qui atteindra toutes les communaut&eacute;s perdues autour de nous. Nous faisons confiance &agrave; Dieu pour nous utiliser pour apporter &laquo; une &eacute;glise &agrave; chaque village et communaut&eacute; et l&#39;&eacute;vangile &agrave; chaque personne! &raquo;</p>

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

<p>De grandes foules commen&ccedil;aient &agrave; suivre J&eacute;sus. Ils ont entendu parler des gu&eacute;risons miraculeuses et de la nourriture pourvue aux multitudes. Ils &eacute;taient attir&eacute;s par Lui &agrave; cause des b&eacute;n&eacute;fices qu&#39;ils esp&eacute;raient recevoir de Lui. Mais J&eacute;sus connaissait leurs c&oelig;urs. Il savait qu&#39;ils ne voulaient vraiment pas le suivre inconditionnellement. Il voulait qu&#39;ils reconnaissent que Le suivre signifiait Lui abandonner tout.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 14:25-33 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 14:25-33</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">25&nbsp;</sup>De grandes foules faisaient route avec J&eacute;sus. Il se retourna, et leur dit:</p>

<p><sup class="versenum">26&nbsp;</sup>Si quelqu&#39;un vient &agrave; moi, et s&#39;il ne hait pas son p&egrave;re, sa m&egrave;re, sa femme, ses enfants, ses fr&egrave;res, et ses soeurs, et m&ecirc;me &agrave; sa propre vie, il ne peut &ecirc;tre mon disciple.</p>

<p><sup class="versenum">27&nbsp;</sup>Et quiconque ne porte pas sa croix, et ne me suis pas, ne peut &ecirc;tre mon disciple.</p>

<p><sup class="versenum">28&nbsp;</sup>Car, lequel de vous, s&#39;il veut b&acirc;tir une tour, ne s&#39;assied d&#39;abord pour calculer la d&eacute;pense et voir s&#39;il a de quoi la terminer,</p>

<p><sup class="versenum">29&nbsp;</sup>de peur qu&#39;apr&egrave;s avoir pos&eacute; les fondements, il ne puisse l&#39;achever, et que tous ceux qui le verront ne se mettent &agrave; le railler,</p>

<p><sup class="versenum">30&nbsp;</sup>en disant: Cet homme a commenc&eacute; &agrave; b&acirc;tir, et il n&#39;a pu achever?</p>

<p><sup class="versenum">31&nbsp;</sup>Ou quel roi, s&#39;il va faire la guerre &agrave; un autre roi, ne s&#39;assied d&#39;abord pour examiner s&#39;il peut, avec dix mille hommes, marcher &agrave; la rencontre de celui qui vient l&#39;attaquer avec vingt mille?</p>

<p><sup class="versenum">32&nbsp;</sup>S&#39;il ne le peut, tandis que cet autre roi est encore loin, il lui envoie une ambassade pour demander la paix.</p>

<p><sup class="versenum">33&nbsp;</sup>Ainsi donc, quiconque d&#39;entre vous ne renonce pas &agrave; tout ce qu&#39;il poss&egrave;de ne peut &ecirc;tre mon disciple.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/116.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 14:25-33&nbsp; </button>
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

<p>Lorsque nous suivons Christ, les bienfaits sont &eacute;ternels et incomparables: le pardon des p&eacute;ch&eacute;s, le salut et la s&eacute;curit&eacute; dans le Roi des Rois et le Seigneur des Seigneurs. Mais &ecirc;tre un disciple de J&eacute;sus ne vous &eacute;pargnera pas de peine et d&#39;&eacute;preuves. Parce que nous vivons dans un monde mauvais, suivre Christ vous apportera aussi la pers&eacute;cution et les d&eacute;fis. Quiconque d&eacute;sire vivre une vie pieuse en J&eacute;sus sera pers&eacute;cut&eacute; par les autres. Mais soyons encourag&eacute;s par Pierre, l&#39;un des amis les plus proches de J&eacute;sus, lisez <span class="popup-link" @click = "popUp('pop4')"> 1 Pierre 4:12-19</span>.&nbsp;</p>

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">12&nbsp;</sup>Bien-aim&eacute;s, ne soyez pas surpris, comme d&#39;une chose &eacute;trange qui vous arrive, de la fournaise qui est au milieu de vous pour vous &eacute;prouver.</p>

<p><sup class="versenum">13&nbsp;</sup>R&eacute;jouissez-vous, au contraire, de la part que vous avez aux souffrances de Christ, afin que vous soyez aussi dans la joie et dans l&#39;all&eacute;gresse lorsque sa gloire appara&icirc;tra.</p>

<p><sup class="versenum">14&nbsp;</sup>Si vous &ecirc;tes outrag&eacute;s pour le nom de Christ, vous &ecirc;tes heureux, parce que l&#39;Esprit de gloire, l&#39;Esprit de Dieu, repose sur vous.</p>

<p><sup class="versenum">15&nbsp;</sup>Que nul de vous, en effet, ne souffre comme meurtrier, ou voleur, ou malfaiteur, ou comme s&#39;ing&eacute;rant dans les affaires d&#39;autrui.</p>

<p><sup class="versenum">16&nbsp;</sup>Mais si quelqu&#39;un souffre comme chr&eacute;tien, qu&#39;il n&#39;en ait point honte, et que plut&ocirc;t il glorifie Dieu &agrave; cause de ce nom.</p>

<p><sup class="versenum">17&nbsp;</sup>Car c&#39;est le moment o&ugrave; le jugement va commencer par la maison de Dieu. Or, si c&#39;est par nous qu&#39;il commence, quelle sera la fin de ceux qui n&#39;ob&eacute;issent pas &agrave; l&#39;&Eacute;vangile de Dieu?</p>

<p><sup class="versenum">18&nbsp;</sup>Et si le juste se sauve avec peine, que deviendront l&#39;impie et le p&eacute;cheur?</p>

<p><sup class="versenum">19&nbsp;</sup>Ainsi, que ceux qui souffrent selon la volont&eacute; de Dieu remettent leurs &acirc;mes au fid&egrave;le Cr&eacute;ateur, en faisant ce qui est bien.</p>
<!-- end bible --></div>

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
	<li>Pratiquez n&#39;importe quelle comp&eacute;tence ou sujet des le&ccedil;ons pr&eacute;c&eacute;dentes pour aider &agrave; se pr&eacute;parer &agrave; servir les autres</li>
	<li>Pratiquez la lib&eacute;ralit&eacute;, comme convenu.</li>
	<li>Souvenez-vous du sacrifice de J&eacute;sus par la sainte c&egrave;ne, le cas &eacute;ch&eacute;ant.</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>Ecrivez des promesses &laquo; Je le ferai d&rsquo;ici quand &raquo; et dites les &agrave; votre petit groupe.</li>
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

			<td class="social" @click="share('lesson', 'Coût du Discipôlat: ', '/content/M2/fra/multiply1/multiply116.html')">
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