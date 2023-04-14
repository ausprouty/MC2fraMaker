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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<h1>Période 2: Le cœur de Jésus pour tout le monde (les barrières interculturelles)</h1>
<div id="showVideoOptions"></div>
  <h2>Le c&oelig;ur de J&eacute;sus pour tout le monde (les barri&egrave;res interculturelles)</h2>

<p class="year">[32-45 ap .J.-C.]</p>

<h2>R&eacute;sum&eacute;&nbsp;</h2>

<p>Cette p&eacute;riode couvre environ 12 ann&eacute;es de croissances et de minist&egrave;re. Elle est marqu&eacute;e par le passage de nouvelles barri&egrave;res &nbsp;culturelles lorsque J&eacute;sus &nbsp;oriente les croyants &agrave; aller en dehors de J&eacute;rusalem pour faire des disciples. Faire des disciples et l&rsquo;implantation d&rsquo;&eacute;glise se r&eacute;pandaient de J&eacute;rusalem dans la Jud&eacute;e, la Samarie et dans le monde Pa&iuml;en.</p>

<h2><br />
Les lettres &eacute;crites &nbsp;pendant cette p&eacute;riode</h2>

<ul>
	<li>
	<p>Jacques, au milieu des ann&eacute;es 40<br />
	&nbsp;</p>
	</li>
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

			<td class="social" @click="share('lesson', 'Période 2: Le cœur de Jésus pour tout le monde (les barrières interculturelles): ', '/content/M2/fra/multiply3/multiply3intro2.html')">
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