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
                        <div class="chapter_number ltr"><h1>10.</h1></div>
                        <div class="chapter_title ltr"><h1>La Passion Révélée au Temple</h1></div>
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
	<li>Lisez ou observez Jean 2:12-25 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 2:12-25</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>Apr&egrave;s cela, il descendit &agrave; Caperna&uuml;m, avec sa m&egrave;re, ses fr&egrave;res et ses disciples, et ils n&#39;y demeur&egrave;rent que peu de jours.</p>

<p><sup class="versenum">13&nbsp;</sup>La P&acirc;que des Juifs &eacute;tait proche, et J&eacute;sus monta &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">14&nbsp;</sup>Il trouva dans le temple les vendeurs de boeufs, de brebis et de pigeons, et les changeurs assis.</p>

<p><sup class="versenum">15&nbsp;</sup>Ayant fait un fouet avec des cordes, il les chassa tous du temple, ainsi que les brebis et les boeufs; il dispersa la monnaie des changeurs, et renversa les tables;</p>

<p><sup class="versenum">16&nbsp;</sup>et il dit aux vendeurs de pigeons: Otez cela d&#39;ici, ne faites pas de la maison de mon P&egrave;re une maison de trafic.</p>

<p><sup class="versenum">17&nbsp;</sup>Ses disciples se souvinrent qu&#39;il est &eacute;crit: Le z&egrave;le de ta maison me d&eacute;vore.</p>

<p><sup class="versenum">18&nbsp;</sup>Les Juifs, prenant la parole, lui dirent: Quel miracle nous montres-tu, pour agir de la sorte?</p>

<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: D&eacute;truisez ce temple, et en trois jours je le rel&egrave;verai.</p>

<p><sup class="versenum">20&nbsp;</sup>Les Juifs dirent: Il a fallu quarante-six ans pour b&acirc;tir ce temple, et toi, en trois jours tu le rel&egrave;veras!</p>

<p><sup class="versenum">21&nbsp;</sup>Mais il parlait du temple de son corps.</p>

<p><sup class="versenum">22&nbsp;</sup>C&#39;est pourquoi, lorsqu&#39;il fut ressuscit&eacute; des morts, ses disciples se souvinrent qu&#39;il avait dit cela, et ils crurent &agrave; l&#39;&Eacute;criture et &agrave; la parole que J&eacute;sus avait dite.</p>

<p><sup class="versenum">23&nbsp;</sup>Pendant que J&eacute;sus &eacute;tait &agrave; J&eacute;rusalem, &agrave; la f&ecirc;te de P&acirc;que, plusieurs crurent en son nom, voyant les miracles qu&#39;il faisait.</p>

<p><sup class="versenum">24&nbsp;</sup>Mais J&eacute;sus ne se fiait point &agrave; eux, parce qu&#39;il les connaissait tous,</p>

<p><sup class="versenum">25&nbsp;</sup>et parce qu&#39;il n&#39;avait pas besoin qu&#39;on lui rend&icirc;t t&eacute;moignage d&#39;aucun homme; car il savait lui-m&ecirc;me ce qui &eacute;tait dans l&#39;homme.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/210.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 2:12-25&nbsp; </button>
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

<p>J&eacute;sus emm&egrave;ne ses disciples &agrave; J&eacute;rusalem pour la f&ecirc;te de la P&acirc;que. C&#39;&eacute;tait un festival de sept jours pour c&eacute;l&eacute;brer la d&eacute;livrance d&#39;Isra&euml;l d&#39;Egypte sous la direction de Mo&iuml;se. Nous voyons la passion de J&eacute;sus pour le nom et la r&eacute;putation du P&egrave;re. Il &eacute;tait f&acirc;ch&eacute; que l&#39;attention du peuple ait &eacute;t&eacute; d&eacute;tourn&eacute;e de l&rsquo;adoration du P&egrave;re et de profiter des gens pour gagner de l&#39;argent. Nous voyons ici de vraies &eacute;motions humaines d&#39;un vrai J&eacute;sus humain; nous voyons du vrai courage d&#39;un vrai J&eacute;sus divin, qui aimait si tant le P&egrave;re qu&#39;il ne pouvait pas rester l&agrave; et voir les gens gagner de l&#39;argent &agrave; partir de ce que Dieu offrait comme un don gratuit.</p>

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

			<td class="social" @click="share('lesson', 'La Passion Révélée au Temple: ', '/content/M2/fra/multiply2/multiply210.html')">
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