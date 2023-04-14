<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"
import VueImageZoomer from '@/components/VueImageZoomer.vue'
import '@/assets/styles/vueImageZoomer.css';


export default {
  components: {
    VueImageZoomer
  },
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
<h1>Période 1 Résumé de la préparation</h1>
<div id="showVideoOptions"></div>
  <h2>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="/images/zoom/sites/mc2/content/M2/fra/multiply2/period1.png" 
    zoom="/images/zoom/sites/mc2/content/M2/fra/multiply2/period1.png" :zoom-amount="3" img-class="img-fluid" alt="Stage of Ministry">
    <img src="@/assets/sites/mc2/content/M2/fra/multiply2/period1.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div></h2>

<p>Devenir la personne que vous cherchez &agrave; multiplier, se pr&eacute;parer pour une vie pieuse et un mouvement de multiplication.</p>

<p>Ceci va de sa naissance autour de 4 av. J.C. jusqu&rsquo;&agrave; environ 30 ans d&rsquo;&acirc;ge.&nbsp;</p>

<ul>
	<li>Au cours des 30 premi&egrave;res ann&eacute;es de sa vie, il &laquo;a grandi et est devenu&raquo; (<span class="popup-link" @click = "popUp('pop1')"> Luc 2:40</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">40&nbsp;</sup>Or, l&#39;enfant croissait et se fortifiait. Il &eacute;tait rempli de sagesse, et la gr&acirc;ce de Dieu &eacute;tait sur lui.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Luc 2:51-52</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">51&nbsp;</sup>Puis il descendit avec eux pour aller &agrave; Nazareth, et il leur &eacute;tait soumis. Sa m&egrave;re gardait toutes ces choses dans son coeur.</p>

	<p><sup class="versenum">52&nbsp;</sup>Et J&eacute;sus croissait en sagesse, en stature, et en gr&acirc;ce, devant Dieu et devant les hommes.</p>
	<!-- end bible --></div>
	&nbsp;le Produit qu&rsquo;il cherchait &agrave; multiplier dans la vie d&rsquo;autres personnes.&nbsp;Ceci est bien avant qu&rsquo;Il ne commence son minist&egrave;re public. La pri&egrave;re, la planification et la clarification de ce que son minist&egrave;re allait &ecirc;tre et comment s&rsquo;y prendre &eacute;taient &eacute;vidents une fois qu&rsquo;il a lanc&eacute; (le minist&egrave;re).<br />
	&nbsp;</li>
	<li>La Passion de son c&oelig;ur &eacute;tait pure, son But &eacute;tait clair, et<br />
	&nbsp;</li>
	<li>Le Processus qu&rsquo;il a d&eacute;cid&eacute; &eacute;tait simple: son travail consistera &agrave; entrer en contact avec les perdus, les gagner &agrave; Lui-m&ecirc;me, les pr&eacute;parer pour le suivre, les former &agrave; en p&ecirc;cher d&rsquo;autres&nbsp; et les envoyer pour Multiplier le m&ecirc;me processus.<br />
	&nbsp;</li>
	<li>Il a d&eacute;cid&eacute; qu&rsquo;il cherchera, travaillera avec et par Ceux que le P&egrave;re a pr&eacute;par&eacute;.</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Période 1 Résumé de la préparation: ', '/content/M2/fra/multiply2/multiply2intro1.html')">
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