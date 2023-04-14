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
                        <div class="chapter_number ltr"><h1>24.</h1></div>
                        <div class="chapter_title ltr"><h1>Dire la verité</h1></div>
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
	<li>Lisez ou observez Jean 5:1-17 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 5:1-17</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s cela, il y eut une f&ecirc;te des Juifs, et J&eacute;sus monta &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">2&nbsp;</sup>Or, &agrave; J&eacute;rusalem, pr&egrave;s de la porte des brebis, il y a une piscine qui s&#39;appelle en h&eacute;breu B&eacute;thesda, et qui a cinq portiques.</p>

<p><sup class="versenum">3&nbsp;</sup>Sous ces portiques &eacute;taient couch&eacute;s en grand nombre des malades, des aveugles, des boiteux, des paralytiques, qui attendaient le mouvement de l&#39;eau;</p>

<p><sup class="versenum">4&nbsp;</sup>car un ange descendait de temps en temps dans la piscine, et agitait l&#39;eau; et celui qui y descendait le premier apr&egrave;s que l&#39;eau avait &eacute;t&eacute; agit&eacute;e &eacute;tait gu&eacute;ri, quelle que f&ucirc;t sa maladie.</p>

<p><sup class="versenum">5&nbsp;</sup>L&agrave; se trouvait un homme malade depuis trente-huit ans.</p>

<p><sup class="versenum">6&nbsp;</sup>J&eacute;sus, l&#39;ayant vu couch&eacute;, et sachant qu&#39;il &eacute;tait malade depuis longtemps, lui dit: Veux-tu &ecirc;tre gu&eacute;ri?</p>

<p><sup class="versenum">7&nbsp;</sup>Le malade lui r&eacute;pondit: Seigneur, je n&#39;ai personne pour me jeter dans la piscine quand l&#39;eau est agit&eacute;e, et, pendant que j&#39;y vais, un autre descend avant moi.</p>

<p><sup class="versenum">8&nbsp;</sup>L&egrave;ve-toi, lui dit J&eacute;sus, prends ton lit, et marche.</p>

<p><sup class="versenum">9&nbsp;</sup>Aussit&ocirc;t cet homme fut gu&eacute;ri; il prit son lit, et marcha.</p>

<p><sup class="versenum">10&nbsp;</sup>C&#39;&eacute;tait un jour de sabbat. Les Juifs dirent donc &agrave; celui qui avait &eacute;t&eacute; gu&eacute;ri: C&#39;est le sabbat; il ne t&#39;est pas permis d&#39;emporter ton lit.</p>

<p><sup class="versenum">11&nbsp;</sup>Il leur r&eacute;pondit: Celui qui m&#39;a gu&eacute;ri m&#39;a dit: Prends ton lit, et marche.</p>

<p><sup class="versenum">12&nbsp;</sup>Ils lui demand&egrave;rent: Qui est l&#39;homme qui t&#39;a dit: Prends ton lit, et marche?</p>

<p><sup class="versenum">13&nbsp;</sup>Mais celui qui avait &eacute;t&eacute; gu&eacute;ri ne savait pas qui c&#39;&eacute;tait; car J&eacute;sus avait disparu de la foule qui &eacute;tait en ce lieu.</p>

<p><sup class="versenum">14&nbsp;</sup>Depuis, J&eacute;sus le trouva dans le temple, et lui dit: Voici, tu as &eacute;t&eacute; gu&eacute;ri; ne p&egrave;che plus, de peur qu&#39;il ne t&#39;arrive quelque chose de pire.</p>

<p><sup class="versenum">15&nbsp;</sup>Cet homme s&#39;en alla, et annon&ccedil;a aux Juifs que c&#39;&eacute;tait J&eacute;sus qui l&#39;avait gu&eacute;ri.</p>

<p><sup class="versenum">16&nbsp;</sup>C&#39;est pourquoi les Juifs poursuivaient J&eacute;sus, parce qu&#39;il faisait ces choses le jour du sabbat.</p>

<p><sup class="versenum">17&nbsp;</sup>Mais J&eacute;sus leur r&eacute;pondit: Mon P&egrave;re agit jusqu&#39;&agrave; pr&eacute;sent; moi aussi, j&#39;agis.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/224.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 5:1-17&nbsp; </button>
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

<p>J&eacute;sus fait un autre long voyage jusqu&#39;&agrave; J&eacute;rusalem pour un autre festin. Son dernier voyage &agrave; J&eacute;rusalem pour une f&ecirc;te a provoqu&eacute; une grande agitation et la m&ecirc;me chose s&#39;est encore produite. Cette fois, le P&egrave;re conduisit J&eacute;sus &agrave; une piscine juste &agrave; l&#39;ext&eacute;rieur de l&#39;une des portes de la ville appel&eacute;e Porte des brebis, o&ugrave; se trouvaient couch&eacute;s des malades en grand nombre. J&eacute;sus a seulement gu&eacute;ri celui vers qui le P&egrave;re l&#39;avait conduit. Parce que cela a &eacute;t&eacute; fait un jour de sabbat (jour de repos), les chefs religieux &eacute;taient tr&egrave;s contrari&eacute;s et ont pers&eacute;cut&eacute; J&eacute;sus. J&eacute;sus a profit&eacute; de l&#39;occasion pour r&eacute;v&eacute;ler sa relation unique avec le P&egrave;re. Les Juifs ont clairement compris que J&eacute;sus pr&eacute;tendait &ecirc;tre &eacute;gal &agrave; Dieu et &agrave; partir de ce moment, ils cherchent un moyen de le tuer.</p>

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

			<td class="social" @click="share('lesson', 'Dire la verité: ', '/content/M2/fra/multiply2/multiply224.html')">
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