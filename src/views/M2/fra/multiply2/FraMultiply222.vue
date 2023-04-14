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
                        <div class="chapter_number ltr"><h1>22.</h1></div>
                        <div class="chapter_title ltr"><h1>Cinquième Expédition de la Pêche d’hommes</h1></div>
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
	<li>Lisez ou observez Luc 5:17-26 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 5:17-26</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">17&nbsp;</sup>Un jour J&eacute;sus enseignait. Des pharisiens et des docteurs de la loi &eacute;taient l&agrave; assis, venus de tous les villages de la Galil&eacute;e, de la Jud&eacute;e et de J&eacute;rusalem; et la puissance du Seigneur se manifestait par des gu&eacute;risons.</p>

<p><sup class="versenum">18&nbsp;</sup>Et voici, des gens, portant sur un lit un homme qui &eacute;tait paralytique, cherchaient &agrave; le faire entrer et &agrave; le placer sous ses regards.</p>

<p><sup class="versenum">19&nbsp;</sup>Comme ils ne savaient par o&ugrave; l&#39;introduire, &agrave; cause de la foule, ils mont&egrave;rent sur le toit, et ils le descendirent par une ouverture, avec son lit, au milieu de l&#39;assembl&eacute;e, devant J&eacute;sus.</p>

<p><sup class="versenum">20&nbsp;</sup>Voyant leur foi, J&eacute;sus dit: Homme, tes p&eacute;ch&eacute;s te sont pardonn&eacute;s.</p>

<p><sup class="versenum">21&nbsp;</sup>Les scribes et les pharisiens se mirent &agrave; raisonner et &agrave; dire: Qui est celui-ci, qui prof&egrave;re des blasph&egrave;mes? Qui peut pardonner les p&eacute;ch&eacute;s, si ce n&#39;est Dieu seul?</p>

<p><sup class="versenum">22&nbsp;</sup>J&eacute;sus, connaissant leurs pens&eacute;es, prit la parole et leur dit: Quelles pens&eacute;es avez-vous dans vos coeurs?</p>

<p><sup class="versenum">23&nbsp;</sup>Lequel est le plus ais&eacute;, de dire: Tes p&eacute;ch&eacute;s te sont pardonn&eacute;s, ou de dire: L&egrave;ve-toi, et marche?</p>

<p><sup class="versenum">24&nbsp;</sup>Or, afin que vous sachiez que le Fils de l&#39;homme a sur la terre le pouvoir de pardonner les p&eacute;ch&eacute;s: Je te l&#39;ordonne, dit-il au paralytique, l&egrave;ve-toi, prends ton lit, et va dans ta maison.</p>

<p><sup class="versenum">25&nbsp;</sup>Et, &agrave; l&#39;instant, il se leva en leur pr&eacute;sence, prit le lit sur lequel il &eacute;tait couch&eacute;, et s&#39;en alla dans sa maison, glorifiant Dieu.</p>

<p><sup class="versenum">26&nbsp;</sup>Tous &eacute;taient dans l&#39;&eacute;tonnement, et glorifiaient Dieu; remplis de crainte, ils disaient: Nous avons vu aujourd&#39;hui des choses &eacute;tranges.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/222.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 5:17-26&nbsp; </button>
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

<p>Le mouvement est en croissance. Des foules venues de partout venaient l&#39;entendre et &ecirc;tre gu&eacute;ries. La gu&eacute;rison de l&#39;homme atteint de la l&egrave;pre avait amen&eacute; des pharisiens et des docteurs de la loi de tous les villages de Galil&eacute;e et de Jud&eacute;e et J&eacute;rusalem &agrave; se r&eacute;unir pour en savoir plus sur cet homme qui avait gu&eacute;ri un l&eacute;preux. &Agrave; cette occasion, J&eacute;sus gu&eacute;rissait beaucoup par la puissance de l&#39;Esprit. Quatre amis ont hardiment forc&eacute; leur chemin vers le devant de la foule pour amener leur ami paralys&eacute; &agrave; J&eacute;sus. Il a utilis&eacute; la situation pour t&eacute;moigner aux chefs religieux qui Il est r&eacute;ellement. En pardonnant les p&eacute;ch&eacute;s de l&#39;homme, J&eacute;sus se montre &eacute;gal avec Dieu. Tous ceux qui ont vu la gu&eacute;rison ont donn&eacute; gloire au P&egrave;re.</p>

<ul>
	<li class="nobreak-final-final">Etude approfondie: <span class="popup-link" @click = "popUp('pop1')">  Matthieu 9:1-8</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>J&eacute;sus, &eacute;tant mont&eacute; dans une barque, traversa la mer, et alla dans sa ville.</p>

	<p><sup class="versenum">2&nbsp;</sup>Et voici, on lui amena un paralytique couch&eacute; sur un lit. J&eacute;sus, voyant leur foi, dit au paralytique: Prends courage, mon enfant, tes p&eacute;ch&eacute;s te sont pardonn&eacute;s.</p>

	<p><sup class="versenum">3&nbsp;</sup>Sur quoi, quelques scribes dirent au dedans d&#39;eux: Cet homme blasph&egrave;me.</p>

	<p><sup class="versenum">4&nbsp;</sup>Et J&eacute;sus, connaissant leurs pens&eacute;es, dit: Pourquoi avez-vous de mauvaises pens&eacute;es dans vos coeurs?</p>

	<p><sup class="versenum">5&nbsp;</sup>Car, lequel est le plus ais&eacute;, de dire: Tes p&eacute;ch&eacute;s sont pardonn&eacute;s, ou de dire: L&egrave;ve-toi, et marche?</p>

	<p><sup class="versenum">6&nbsp;</sup>Or, afin que vous sachiez que le Fils de l&#39;homme a sur la terre le pouvoir de pardonner les p&eacute;ch&eacute;s: L&egrave;ve-toi, dit-il au paralytique, prends ton lit, et va dans ta maison.</p>

	<p><sup class="versenum">7&nbsp;</sup>Et il se leva, et s&#39;en alla dans sa maison.</p>

	<p><sup class="versenum">8&nbsp;</sup>Quand la foule vit cela, elle fut saisie de crainte, et elle glorifia Dieu, qui a donn&eacute; aux hommes un tel pouvoir.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Marc 2:1-13</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Quelques jours apr&egrave;s, J&eacute;sus revint &agrave; Caperna&uuml;m. On apprit qu&#39;il &eacute;tait &agrave; la maison,</p>

	<p><sup class="versenum">2&nbsp;</sup>et il s&#39;assembla un si grand nombre de personnes que l&#39;espace devant la porte ne pouvait plus les contenir. Il leur annon&ccedil;ait la parole.</p>

	<p><sup class="versenum">3&nbsp;</sup>Des gens vinrent &agrave; lui, amenant un paralytique port&eacute; par quatre hommes.</p>

	<p><sup class="versenum">4&nbsp;</sup>Comme ils ne pouvaient l&#39;aborder, &agrave; cause de la foule, ils d&eacute;couvrirent le toit de la maison o&ugrave; il &eacute;tait, et ils descendirent par cette ouverture le lit sur lequel le paralytique &eacute;tait couch&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>J&eacute;sus, voyant leur foi, dit au paralytique: Mon enfant, tes p&eacute;ch&eacute;s sont pardonn&eacute;s.</p>

	<p><sup class="versenum">6&nbsp;</sup>Il y avait l&agrave; quelques scribes, qui &eacute;taient assis, et qui se disaient au dedans d&#39;eux:</p>

	<p><sup class="versenum">7&nbsp;</sup>Comment cet homme parle-t-il ainsi? Il blasph&egrave;me. Qui peut pardonner les p&eacute;ch&eacute;s, si ce n&#39;est Dieu seul?</p>

	<p><sup class="versenum">8&nbsp;</sup>J&eacute;sus, ayant aussit&ocirc;t connu par son esprit ce qu&#39;ils pensaient au dedans d&#39;eux, leur dit: Pourquoi avez-vous de telles pens&eacute;es dans vos coeurs?</p>

	<p><sup class="versenum">9&nbsp;</sup>Lequel est le plus ais&eacute;, de dire au paralytique: Tes p&eacute;ch&eacute;s sont pardonn&eacute;s, ou de dire: L&egrave;ve-toi, prends ton lit, et marche?</p>

	<p><sup class="versenum">10&nbsp;</sup>Or, afin que vous sachiez que le Fils de l&#39;homme a sur la terre le pouvoir de pardonner les p&eacute;ch&eacute;s:</p>

	<p><sup class="versenum">11&nbsp;</sup>Je te l&#39;ordonne, dit-il au paralytique, l&egrave;ve-toi, prends ton lit, et va dans ta maison.</p>

	<p><sup class="versenum">12&nbsp;</sup>Et, &agrave; l&#39;instant, il se leva, prit son lit, et sortit en pr&eacute;sence de tout le monde, de sorte qu&#39;ils &eacute;taient tous dans l&#39;&eacute;tonnement et glorifiaient Dieu, disant: Nous n&#39;avons jamais rien vu de pareil.</p>

	<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus sortit de nouveau du c&ocirc;t&eacute; de la mer. Toute la foule venait &agrave; lui, et il les enseignait.</p>
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

			<td class="social" @click="share('lesson', 'Cinquième Expédition de la Pêche d’hommes: ', '/content/M2/fra/multiply2/multiply222.html')">
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