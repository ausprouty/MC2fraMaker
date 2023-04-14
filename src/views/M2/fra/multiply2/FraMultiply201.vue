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
                        <div class="chapter_number ltr"><h1>1.</h1></div>
                        <div class="chapter_title ltr"><h1>Jésus, pleinement Dieu est devenu pleinement homme</h1></div>
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
	<li>Lisez ou observez Jean 1:1-14 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 1:1-14</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Au commencement &eacute;tait la Parole, et la Parole &eacute;tait avec Dieu, et la Parole &eacute;tait Dieu.</p>

<p><sup class="versenum">2&nbsp;</sup>Elle &eacute;tait au commencement avec Dieu.</p>

<p><sup class="versenum">3&nbsp;</sup>Toutes choses ont &eacute;t&eacute; faites par elle, et rien de ce qui a &eacute;t&eacute; fait n&#39;a &eacute;t&eacute; fait sans elle.</p>

<p><sup class="versenum">4&nbsp;</sup>En elle &eacute;tait la vie, et la vie &eacute;tait la lumi&egrave;re des hommes.</p>

<p><sup class="versenum">5&nbsp;</sup>La lumi&egrave;re luit dans les t&eacute;n&egrave;bres, et les t&eacute;n&egrave;bres ne l&#39;ont point re&ccedil;ue.</p>

<p><sup class="versenum">6&nbsp;</sup>Il y eut un homme envoy&eacute; de Dieu: son nom &eacute;tait Jean.</p>

<p><sup class="versenum">7&nbsp;</sup>Il vint pour servir de t&eacute;moin, pour rendre t&eacute;moignage &agrave; la lumi&egrave;re, afin que tous crussent par lui.</p>

<p><sup class="versenum">8&nbsp;</sup>Il n&#39;&eacute;tait pas la lumi&egrave;re, mais il parut pour rendre t&eacute;moignage &agrave; la lumi&egrave;re.</p>

<p><sup class="versenum">9&nbsp;</sup>Cette lumi&egrave;re &eacute;tait la v&eacute;ritable lumi&egrave;re, qui, en venant dans le monde, &eacute;claire tout homme.</p>

<p><sup class="versenum">10&nbsp;</sup>Elle &eacute;tait dans le monde, et le monde a &eacute;t&eacute; fait par elle, et le monde ne l&#39;a point connue.</p>

<p><sup class="versenum">11&nbsp;</sup>Elle est venue chez les siens, et les siens ne l&#39;ont point re&ccedil;ue.</p>

<p><sup class="versenum">12&nbsp;</sup>Mais &agrave; tous ceux qui l&#39;ont re&ccedil;ue, &agrave; ceux qui croient en son nom, elle a donn&eacute; le pouvoir de devenir enfants de Dieu, lesquels sont n&eacute;s,</p>

<p><sup class="versenum">13&nbsp;</sup>non du sang, ni de la volont&eacute; de la chair, ni de la volont&eacute; de l&#39;homme, mais de Dieu.</p>

<p><sup class="versenum">14&nbsp;</sup>Et la parole a &eacute;t&eacute; faite chair, et elle a habit&eacute; parmi nous, pleine de gr&acirc;ce et de v&eacute;rit&eacute;; et nous avons contempl&eacute; sa gloire, une gloire comme la gloire du Fils unique venu du P&egrave;re.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/201.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 1:1-14&nbsp; </button>
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

<p>Lisez <span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:5-11</span>.&nbsp;</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">5&nbsp;</sup>Ayez en vous les sentiments qui &eacute;taient en J&eacute;sus Christ,</p>

<p><sup class="versenum">6&nbsp;</sup>lequel, existant en forme de Dieu, n&#39;a point regard&eacute; comme une proie &agrave; arracher d&#39;&ecirc;tre &eacute;gal avec Dieu,</p>

<p><sup class="versenum">7&nbsp;</sup>mais s&#39;est d&eacute;pouill&eacute; lui-m&ecirc;me, en prenant une forme de serviteur, en devenant semblable aux hommes; et ayant paru comme un simple homme,</p>

<p><sup class="versenum">8&nbsp;</sup>il s&#39;est humili&eacute; lui-m&ecirc;me, se rendant ob&eacute;issant jusqu&#39;&agrave; la mort, m&ecirc;me jusqu&#39;&agrave; la mort de la croix.</p>

<p><sup class="versenum">9&nbsp;</sup>C&#39;est pourquoi aussi Dieu l&#39;a souverainement &eacute;lev&eacute;, et lui a donn&eacute; le nom qui est au-dessus de tout nom,</p>

<p><sup class="versenum">10&nbsp;</sup>afin qu&#39;au nom de J&eacute;sus tout genou fl&eacute;chisse dans les cieux, sur la terre et sous la terre,</p>

<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
<!-- end bible --></div>
Dieu tout puissant a pris une forme humaine. Il a choisi commencer comme un b&eacute;b&eacute; et non comme un homme adulte. La Bible dit qu&rsquo;il &laquo; s&rsquo;est d&eacute;pouill&eacute; lui- m&ecirc;me &raquo; et s&rsquo;est v&ecirc;tu d&rsquo;un corps pour vivre avec nous. Cependant, il n&rsquo;a jamais cess&eacute; d&rsquo;&ecirc;tre pleinement Dieu. Il &eacute;tait toujours omnipotent, omniscient et omnipr&eacute;sent. Malgr&eacute; cela, il a voil&eacute; sa divinit&eacute; et S&rsquo;est intentionnellement limit&eacute; lui-m&ecirc;me ainsi que ses pouvoirs pour devenir un vrai homme.

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

			<td class="social" @click="share('lesson', 'Jésus, pleinement Dieu est devenu pleinement homme: ', '/content/M2/fra/multiply2/multiply201.html')">
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