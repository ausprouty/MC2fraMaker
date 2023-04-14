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
                        <div class="chapter_number ltr"><h1>11.</h1></div>
                        <div class="chapter_title ltr"><h1>Une enquête de nuit</h1></div>
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
	<li>Lisez ou observez Jean 3:1-21 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 3:1-21</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Mais il y eut un homme d&#39;entre les pharisiens, nomm&eacute; Nicod&egrave;me, un chef des Juifs,</p>

<p><sup class="versenum">2&nbsp;</sup>qui vint, lui, aupr&egrave;s de J&eacute;sus, de nuit, et lui dit: Rabbi, nous savons que tu es un docteur venu de Dieu; car personne ne peut faire ces miracles que tu fais, si Dieu n&#39;est avec lui.</p>

<p><sup class="versenum">3&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je te le dis, si un homme ne na&icirc;t de nouveau, il ne peut voir le royaume de Dieu.</p>

<p><sup class="versenum">4&nbsp;</sup>Nicod&egrave;me lui dit: Comment un homme peut-il na&icirc;tre quand il est vieux? Peut-il rentrer dans le sein de sa m&egrave;re et na&icirc;tre?</p>

<p><sup class="versenum">5&nbsp;</sup>J&eacute;sus r&eacute;pondit: En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je te le dis, si un homme ne na&icirc;t d&#39;eau et d&#39;Esprit, il ne peut entrer dans le royaume de Dieu.</p>

<p><sup class="versenum">6&nbsp;</sup>Ce qui est n&eacute; de la chair est chair, et ce qui est n&eacute; de l&#39;Esprit est Esprit.</p>

<p><sup class="versenum">7&nbsp;</sup>Ne t&#39;&eacute;tonne pas que je t&#39;aie dit: Il faut que vous naissiez de nouveau.</p>

<p><sup class="versenum">8&nbsp;</sup>Le vent souffle o&ugrave; il veut, et tu en entends le bruit; mais tu ne sais d&#39;o&ugrave; il vient, ni o&ugrave; il va. Il en est ainsi de tout homme qui est n&eacute; de l&#39;Esprit.</p>

<p><sup class="versenum">9&nbsp;</sup>Nicod&egrave;me lui dit: Comment cela peut-il se faire?</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Tu es le docteur d&#39;Isra&euml;l, et tu ne sais pas ces choses!</p>

<p><sup class="versenum">11&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je te le dis, nous disons ce que nous savons, et nous rendons t&eacute;moignage de ce que nous avons vu; et vous ne recevez pas notre t&eacute;moignage.</p>

<p><sup class="versenum">12&nbsp;</sup>Si vous ne croyez pas quand je vous ai parl&eacute; des choses terrestres, comment croirez-vous quand je vous parlerai des choses c&eacute;lestes?</p>

<p><sup class="versenum">13&nbsp;</sup>Personne n&#39;est mont&eacute; au ciel, si ce n&#39;est celui qui est descendu du ciel, le Fils de l&#39;homme qui est dans le ciel.</p>

<p><sup class="versenum">14&nbsp;</sup>Et comme Mo&iuml;se &eacute;leva le serpent dans le d&eacute;sert, il faut de m&ecirc;me que le Fils de l&#39;homme soit &eacute;lev&eacute;,</p>

<p><sup class="versenum">15&nbsp;</sup>afin que quiconque croit en lui ait la vie &eacute;ternelle.</p>

<p><sup class="versenum">16&nbsp;</sup>Car Dieu a tant aim&eacute; le monde qu&#39;il a donn&eacute; son Fils unique, afin que quiconque croit en lui ne p&eacute;risse point, mais qu&#39;il ait la vie &eacute;ternelle.</p>

<p><sup class="versenum">17&nbsp;</sup>Dieu, en effet, n&#39;a pas envoy&eacute; son Fils dans le monde pour qu&#39;il juge le monde, mais pour que le monde soit sauv&eacute; par lui.</p>

<p><sup class="versenum">18&nbsp;</sup>Celui qui croit en lui n&#39;est point jug&eacute;; mais celui qui ne croit pas est d&eacute;j&agrave; jug&eacute;, parce qu&#39;il n&#39;a pas cru au nom du Fils unique de Dieu.</p>

<p><sup class="versenum">19&nbsp;</sup>Et ce jugement c&#39;est que, la lumi&egrave;re &eacute;tant venue dans le monde, les hommes ont pr&eacute;f&eacute;r&eacute; les t&eacute;n&egrave;bres &agrave; la lumi&egrave;re, parce que leurs oeuvres &eacute;taient mauvaises.</p>

<p><sup class="versenum">20&nbsp;</sup>Car quiconque fait le mal hait la lumi&egrave;re, et ne vient point &agrave; la lumi&egrave;re, de peur que ses oeuvres ne soient d&eacute;voil&eacute;es;</p>

<p><sup class="versenum">21&nbsp;</sup>mais celui qui agit selon la v&eacute;rit&eacute; vient &agrave; la lumi&egrave;re, afin que ses oeuvres soient manifest&eacute;es, parce qu&#39;elles sont faites en Dieu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/211.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 3:1-21&nbsp; </button>
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
Quand J&eacute;sus a chass&eacute; les changeurs d&#39;argent au temple, Il a attir&eacute; l&#39;attention de tout le monde. Un chef religieux de haut rang nomm&eacute; Nicod&egrave;me est venu enqu&ecirc;ter sur J&eacute;sus. J&eacute;sus le met au d&eacute;fi de ne pas regarder lui-m&ecirc;me et ce qui semble impossible, et le met au d&eacute;fi d&#39;ouvrir ses yeux de foi. J&eacute;sus partage que ce que Nicod&egrave;me pense &ecirc;tre impossible devient possible. En Christ, il peut vivre dans la lumi&egrave;re sans crainte. M&ecirc;me si vous ne pouvez pas voir le vent, vous pouvez voir ses effets. J&eacute;sus dit que c&#39;est la m&ecirc;me chose pour ceux qui sont n&eacute;s dans l&#39;Esprit. Dieu nous a tellement aim&eacute;s qu&#39;Il nous a donn&eacute; un moyen de rena&icirc;tre, d&#39;avoir une nouvelle vie en Lui.

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

			<td class="social" @click="share('lesson', 'Une enquête de nuit: ', '/content/M2/fra/multiply2/multiply211.html')">
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