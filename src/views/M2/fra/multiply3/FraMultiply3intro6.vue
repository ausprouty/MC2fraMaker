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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<h1>Période 6: Représenter le mouvement de Jésus</h1>
<div id="showVideoOptions"></div>
  <h2>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="/images/zoom/sites/mc2/content/M2/fra/multiply3/Trip4.png" 
    zoom="/images/zoom/sites/mc2/content/M2/fra/multiply3/Trip4.png" :zoom-amount="3" img-class="img-fluid" alt="">
    <img src="@/assets/sites/mc2/content/M2/fra/multiply3/Trip4.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div>R&eacute;sum&eacute; de la p&eacute;riode</h2>

<p>Apr&egrave;s avoir pos&eacute; les fondations de 6-7 centres de mouvement &agrave; travers la partie orientale de l&rsquo;empire Romain, le r&ocirc;le de Paul maintenant est de saisir les occasions pour d&eacute;fendre la foi. Cette p&eacute;riode est marqu&eacute;e par de longs voyages, la prison, les circonstances dangereuses et les d&eacute;fenses l&eacute;gales devant les autorit&eacute;s gouvernementales en Jud&eacute;e et &agrave; Rome.</p>

<h2>Les lettres &eacute;crites au cours de cette p&eacute;riode :</h2>

<ul>
	<li>Colossiens, 60-62 ap. J.-C.</li>
	<li>Phil&eacute;mon, 60-62 ap. J.-C.</li>
	<li>Eph&eacute;siens, 60-62 ap. J.-C.</li>
	<li>Philippiens, 60-62 ap. J.-C.</li>
</ul>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Période 6: Représenter le mouvement de Jésus: ', '/content/M2/fra/multiply3/multiply3intro6.html')">
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