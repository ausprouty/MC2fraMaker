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
<h1>Période 3&4 Formation au ministere et campagne elargie</h1>
<div id="showVideoOptions"></div>
  <p>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="/images/zoom/sites/mc2/content/M2/fra/multiply2/period34.png" 
    zoom="/images/zoom/sites/mc2/content/M2/fra/multiply2/period34.png" :zoom-amount="3" img-class="img-fluid" alt="Stage of Ministry">
    <img src="@/assets/sites/mc2/content/M2/fra/multiply2/period34.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div></p>

<p>&nbsp;VERS FIN 27 AP.J.-C &ndash; FIN 28 AP.J.-C.&nbsp;</p>

<p>Recruter, former et mobiliser une &eacute;quipe de mission en croissance pour semer &agrave; une &eacute;chelle plus large et faire de nouveaux disciples.</p>

<ul>
	<li class="nobreak-final-final">P&eacute;riode 3 Formation au Minist&egrave;re: dure de 6-9 mois, en commen&ccedil;ant par le d&eacute;placement de J&eacute;sus &agrave; Capharna&uuml;m et le d&eacute;fi des quatre p&ecirc;cheurs (<span class="popup-link" @click = "popUp('pop1')"> Marc 1:16-20</span>),

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Comme il passait le long de la mer de Galil&eacute;e, il vit Simon et Andr&eacute;, fr&egrave;re de Simon, qui jetaient un filet dans la mer; car ils &eacute;taient p&ecirc;cheurs.</p>

	<p><sup class="versenum">17&nbsp;</sup>J&eacute;sus leur dit: Suivez-moi, et je vous ferai p&ecirc;cheurs d&#39;hommes.</p>

	<p><sup class="versenum">18&nbsp;</sup>Aussit&ocirc;t, ils laiss&egrave;rent leurs filets, et le suivirent.</p>

	<p><sup class="versenum">19&nbsp;</sup>&Eacute;tant all&eacute; un peu plus loin, il vit Jacques, fils de Z&eacute;b&eacute;d&eacute;e, et Jean, son fr&egrave;re, qui, eux aussi, &eacute;taient dans une barque et r&eacute;paraient les filets.</p>

	<p><sup class="versenum">20&nbsp;</sup>Aussit&ocirc;t, il les appela; et, laissant leur p&egrave;re Z&eacute;b&eacute;d&eacute;e dans la barque avec les ouvriers, ils le suivirent.</p>
	<!-- end bible --></div>
	tous ceux qui avaient d&eacute;j&agrave; &eacute;t&eacute; disciples de J&eacute;sus depuis le d&eacute;but, pour changer leur priorit&eacute; et devenir des p&ecirc;cheurs stagiaires d&#39;hommes avec J&eacute;sus. Ils forment une &eacute;quipe de mission initiale avec J&eacute;sus et il ajoute bient&ocirc;t L&eacute;vi (<span class="popup-link" @click = "popUp('pop2')"> Marc 2:13-17</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus sortit de nouveau du c&ocirc;t&eacute; de la mer. Toute la foule venait &agrave; lui, et il les enseignait.</p>

	<p><sup class="versenum">14&nbsp;</sup>En passant, il vit L&eacute;vi, fils d&#39;Alph&eacute;e, assis au bureau des p&eacute;ages. Il lui dit: Suis-moi. L&eacute;vi se leva, et le suivit.</p>

	<p><sup class="versenum">15&nbsp;</sup>Comme J&eacute;sus &eacute;tait &agrave; table dans la maison de L&eacute;vi, beaucoup de publicains et de gens de mauvaise vie se mirent aussi &agrave; table avec lui et avec ses disciples; car ils &eacute;taient nombreux, et l&#39;avaient suivi.</p>

	<p><sup class="versenum">16&nbsp;</sup>Les scribes et les pharisiens, le voyant manger avec les publicains et les gens de mauvaise vie, dirent &agrave; ses disciples: Pourquoi mange-t-il et boit-il avec les publicains et les gens de mauvaise vie?</p>

	<p><sup class="versenum">17&nbsp;</sup>Ce que J&eacute;sus ayant entendu, il leur dit: Ce ne sont pas ceux qui se portent bien qui ont besoin de m&eacute;decin, mais les malades. Je ne suis pas venu appeler des justes, mais des p&eacute;cheurs.</p>
	<!-- end bible --></div>
	et d&#39;autres.</li>
	<li class="nobreak-final-final">P&eacute;riode 4 Campagne Elargie: est parall&egrave;le &agrave; la phase 3 (6-9 mois). En m&ecirc;me temps que J&eacute;sus recrute une &eacute;quipe initiale du minist&egrave;re pour partager le travail de la mission, il cr&eacute;e des opportunit&eacute;s pour leur &#39;formation sur le terrain&#39; &agrave; travers les campagnes locales (<span class="popup-link" @click = "popUp('pop3')"> Marc 1:21-34</span>)
	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">21&nbsp;</sup>Ils se rendirent &agrave; Caperna&uuml;m. Et, le jour du sabbat, J&eacute;sus entra d&#39;abord dans la synagogue, et il enseigna.</p>

	<p><sup class="versenum">22&nbsp;</sup>Ils &eacute;taient frapp&eacute;s de sa doctrine; car il enseignait comme ayant autorit&eacute;, et non pas comme les scribes.</p>

	<p><sup class="versenum">23&nbsp;</sup>Il se trouva dans leur synagogue un homme qui avait un esprit impur, et qui s&#39;&eacute;cria:</p>

	<p><sup class="versenum">24&nbsp;</sup>Qu&#39;y a-t-il entre nous et toi, J&eacute;sus de Nazareth? Tu es venu pour nous perdre. Je sais qui tu es: le Saint de Dieu.</p>

	<p><sup class="versenum">25&nbsp;</sup>J&eacute;sus le mena&ccedil;a, disant: Tais-toi, et sors de cet homme.</p>

	<p><sup class="versenum">26&nbsp;</sup>Et l&#39;esprit impur sortit de cet homme, en l&#39;agitant avec violence, et en poussant un grand cri.</p>

	<p><sup class="versenum">27&nbsp;</sup>Tous furent saisis de stup&eacute;faction, de sorte qu&#39;il se demandaient les uns aux autres: Qu&#39;est-ce que ceci? Une nouvelle doctrine! Il commande avec autorit&eacute; m&ecirc;me aux esprits impurs, et ils lui ob&eacute;issent!</p>

	<p><sup class="versenum">28&nbsp;</sup>Et sa renomm&eacute;e se r&eacute;pandit aussit&ocirc;t dans tous les lieux environnants de la Galil&eacute;e.</p>

	<p><sup class="versenum">29&nbsp;</sup>En sortant de la synagogue, ils se rendirent avec Jacques et Jean &agrave; la maison de Simon et d&#39;Andr&eacute;.</p>

	<p><sup class="versenum">30&nbsp;</sup>La belle-m&egrave;re de Simon &eacute;tait couch&eacute;e, ayant la fi&egrave;vre; et aussit&ocirc;t on parla d&#39;elle &agrave; J&eacute;sus.</p>

	<p><sup class="versenum">31&nbsp;</sup>S&#39;&eacute;tant approch&eacute;, il la fit lever en lui prenant la main, et &agrave; l&#39;instant la fi&egrave;vre la quitta. Puis elle les servit.</p>

	<p><sup class="versenum">32&nbsp;</sup>Le soir, apr&egrave;s le coucher du soleil, on lui amena tous les malades et les d&eacute;moniaques.</p>

	<p><sup class="versenum">33&nbsp;</sup>Et toute la ville &eacute;tait rassembl&eacute;e devant sa porte.</p>

	<p><sup class="versenum">34&nbsp;</sup>Il gu&eacute;rit beaucoup de gens qui avaient diverses maladies; il chassa aussi beaucoup de d&eacute;mons, et il ne permettait pas aux d&eacute;mons de parler, parce qu&#39;ils le connaissaient.</p>
	<!-- end bible --></div>
	et r&eacute;gionales et les campagnes &eacute;largies (<span class="popup-link" @click = "popUp('pop4')"> Marc 1:35- 39</span>).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">35&nbsp;</sup>Vers le matin, pendant qu&#39;il faisait encore tr&egrave;s sombre, il se leva, et sortit pour aller dans un lieu d&eacute;sert, o&ugrave; il pria.</p>

	<p><sup class="versenum">36&nbsp;</sup>Simon et ceux qui &eacute;taient avec lui se mirent &agrave; sa recherche;</p>

	<p><sup class="versenum">37&nbsp;</sup>et, quand ils l&#39;eurent trouv&eacute;, ils lui dirent: Tous te cherchent.</p>

	<p><sup class="versenum">38&nbsp;</sup>Il leur r&eacute;pondit: Allons ailleurs, dans les bourgades voisines, afin que j&#39;y pr&ecirc;che aussi; car c&#39;est pour cela que je suis sorti.</p>

	<p><sup class="versenum">39&nbsp;</sup>Et il alla pr&ecirc;cher dans les synagogues, par toute la Galil&eacute;e, et il chassa les d&eacute;mons.</p>
	<!-- end bible --></div>
	Cela se traduit par une grande acc&eacute;l&eacute;ration et un &eacute;lan du mouvement avec une opposition accrue (<span class="popup-link" @click = "popUp('pop5')"> Marc 3:6</span>)

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">6&nbsp;</sup>Les pharisiens sortirent, et aussit&ocirc;t ils se consult&egrave;rent avec les h&eacute;rodiens sur les moyens de le faire p&eacute;rir.</p>
	<!-- end bible --></div>
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

			<td class="social" @click="share('lesson', 'Période 3&4 Formation au ministere et campagne elargie: ', '/content/M2/fra/multiply2/multiply2intro34.html')">
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