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
<h1>Période 5 Multiplication du Leadership</h1>
<div id="showVideoOptions"></div>
  <p>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="/images/zoom/sites/mc2/content/M2/fra/multiply2/period5.png" 
    zoom="/images/zoom/sites/mc2/content/M2/fra/multiply2/period5.png" :zoom-amount="3" img-class="img-fluid" alt="Stage of Ministry">
    <img src="@/assets/sites/mc2/content/M2/fra/multiply2/period5.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div></p>

<p>Couvre environ une quinzaine de mois, en commen&ccedil;ant par la d&eacute;signation des 12 ap&ocirc;tres comme &eacute;tant effectivement des apprentis leaders au sein du groupe plus large de ceux qui &oelig;uvrent dans le minist&egrave;re et un groupe encore plus important de disciples et de ceux qui Le cherchent (<span class="popup-link" @click = "popUp('pop1')"> Luc 6:12-19</span>).</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">12&nbsp;</sup>En ce temps-l&agrave;, J&eacute;sus se rendit sur la montagne pour prier, et il passa toute la nuit &agrave; prier Dieu.</p>

<p><sup class="versenum">13&nbsp;</sup>Quand le jour parut, il appela ses disciples, et il en choisit douze, auxquels il donna le nom d&#39;ap&ocirc;tres:</p>

<p><sup class="versenum">14&nbsp;</sup>Simon, qu&#39;il nomma Pierre; Andr&eacute;, son fr&egrave;re; Jacques; Jean; Philippe; Barth&eacute;lemy;</p>

<p><sup class="versenum">15&nbsp;</sup>Matthieu; Thomas; Jacques, fils d&#39;Alph&eacute;e; Simon, appel&eacute; le z&eacute;lote;</p>

<p><sup class="versenum">16&nbsp;</sup>Jude, fils de Jacques; et Judas Iscariot, qui devint tra&icirc;tre.</p>

<p><sup class="versenum">17&nbsp;</sup>Il descendit avec eux, et s&#39;arr&ecirc;ta sur un plateau, o&ugrave; se trouvaient une foule de ses disciples et une multitude de peuple de toute la Jud&eacute;e, de J&eacute;rusalem, et de la contr&eacute;e maritime de Tyr et de Sidon. Ils &eacute;taient venus pour l&#39;entendre, et pour &ecirc;tre gu&eacute;ris de leurs maladies.</p>

<p><sup class="versenum">18&nbsp;</sup>Ceux qui &eacute;taient tourment&eacute;s par des esprits impurs &eacute;taient gu&eacute;ris.</p>

<p><sup class="versenum">19&nbsp;</sup>Et toute la foule cherchait &agrave; le toucher, parce qu&#39;une force sortait de lui et les gu&eacute;rissait tous.</p>
<!-- end bible --></div>

<p>Les 12 sont clairement des leaders et le fruit de la s&eacute;lection d&eacute;lib&eacute;r&eacute;e de J&eacute;sus, de la d&eacute;signation, de la formation et de Son investissement personnel en eux est attest&eacute; apr&egrave;s la Pentec&ocirc;te &agrave; travers le Livre des Actes. &nbsp;</p>

<ol>
	<li class="nobreak-final-final">Plus tard au cours de cette p&eacute;riode, J&eacute;sus a envoy&eacute; 70 autres (<span class="popup-link" @click = "popUp('pop2')"> Luc 10 :1</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Apr&egrave;s cela, le Seigneur d&eacute;signa encore soixante-dix autres disciples, et il les envoya deux &agrave; deux devant lui dans toutes les villes et dans tous les lieux o&ugrave; lui-m&ecirc;me devait aller.</p>
	<!-- end bible --></div>
	et bien qu&#39;ils ne re&ccedil;urent pas le m&ecirc;me statut formel de leadership dans le r&eacute;cit de l&#39;Evangile, ils furent &eacute;galement envoy&eacute;s comme &laquo; ap&ocirc;tres &raquo; (c.-&agrave;-d. les envoy&eacute;s) et aussi appel&eacute;s &agrave; prier pour la prochaine g&eacute;n&eacute;ration de travailleurs &agrave; travers eux (<span class="popup-link" @click = "popUp('pop3')"> Luc 10: 2</span>).

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Il leur dit: La moisson est grande, mais il y a peu d&#39;ouvriers. Priez donc le ma&icirc;tre de la moisson d&#39;envoyer des ouvriers dans sa moisson.</p>
	<!-- end bible --></div>
	Sans doute beaucoup de ces 70 missionnaires anonymes figuraient dans l&#39;&eacute;glise primitive et parmi les 120 dans la chambre haute et les 500 personnes auxquelles J&eacute;sus s&rsquo;est apparu.</li>
</ol>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Période 5 Multiplication du Leadership: ', '/content/M2/fra/multiply2/multiply2intro5.html')">
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