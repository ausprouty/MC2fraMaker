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
<h1>Période 1: Les conséquences de l’explosion du Royaume en Jérusalem</h1>
<div id="showVideoOptions"></div>
  <ul>
	<li class="nobreak-final-final">Le livre des Actes &eacute;tait &eacute;crit par Luc, comme &eacute;tant une continuit&eacute; de l&rsquo;histoire de J&eacute;sus. Dans l&rsquo;&eacute;vangile selon Luc, il a commenc&eacute; par : &laquo; il m&rsquo;a aussi sembl&eacute; bon, apr&egrave;s avoir fait des recherches exactes sur toutes ces choses depuis leur origine, de te les exposer par &eacute;crit d&rsquo;une mani&egrave;re suivie, excellent Th&eacute;ophile, &raquo; (<span class="popup-link" @click = "popUp('pop1')"> Luc 1 :3</span>; LSG).
	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">3&nbsp;</sup>il m&#39;a aussi sembl&eacute; bon, apr&egrave;s avoir fait des recherches exactes sur toutes ces choses depuis leur origine, de te les exposer par &eacute;crit d&#39;une mani&egrave;re suivie, excellent Th&eacute;ophile,</p>
	<!-- end bible --></div>
	Le livres des actes commence avec la d&eacute;claration, &laquo; Th&eacute;ophile, j&rsquo;ai parl&eacute;, dans mon premier livre, de tout ce que J&eacute;sus a commenc&eacute; de faire et d&rsquo;enseigner d&egrave;s le commencement &raquo; (<span class="popup-link" @click = "popUp('pop2')"> Actes 1 :1</span>; LSG).

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Th&eacute;ophile, j&#39;ai parl&eacute;, dans mon premier livre, de tout ce que J&eacute;sus a commenc&eacute; de faire et d&#39;enseigner d&egrave;s le commencement</p>
	<!-- end bible --></div>
	Le livre des Actes couvre les 30 premi&egrave;res ann&eacute;es de l&rsquo;&eacute;glise (30 &agrave; 62 ap. J.-C.).</li>
</ul>

<h2>Introduction:</h2>

<ul>
	<li class="nobreak-final-final">J&eacute;sus &eacute;tait envoy&eacute; du ciel pour une mission globale du royaume. Il a commenc&eacute; Son minist&egrave;re avec quelques disciples, qui sont venu du minist&egrave;re de Jean-Baptiste. Atteindre toutes les villes d&rsquo;Isra&euml;l, &eacute;tait le plan d&rsquo;action de son travail qu&rsquo;Il a annonc&eacute; (<span class="popup-link" @click = "popUp('pop3')"> Marc 1 :38</span>; LSG)

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">38&nbsp;</sup>Il leur r&eacute;pondit: Allons ailleurs, dans les bourgades voisines, afin que j&#39;y pr&ecirc;che aussi; car c&#39;est pour cela que je suis sorti.</p>
	<!-- end bible --></div>
	mais Il pr&eacute;parait Ses disciples pour plus que cela. Il ne leur a pas seulement enseign&eacute; les v&eacute;rit&eacute;s sur le royaume, mais dans Son humanit&eacute;, il a donn&eacute; &agrave; Ses disciple le mod&egrave;le d&rsquo;une vie centr&eacute;e centr&eacute; et d&eacute;pendante du Saint-Esprit. Le minist&egrave;re de J&eacute;sus s&rsquo;est largement r&eacute;pandu par la s&eacute;lection des leaders et leur autonomisation &agrave; aller vers de nouveaux endroits. Ensuite, avant Sa mort sur la croix, J&eacute;sus a partag&eacute; avec eux le champ d&rsquo;action complet de la mission du royaume, &laquo; Cette bonne nouvelle du royaume sera pr&ecirc;ch&eacute;e dans le monde entier, pour servir de t&eacute;moignage &agrave; toutes les nations. Alors viendra la fin. &raquo; (<span class="popup-link" @click = "popUp('pop4')"> Matthieu 24:14</span>; LSG).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Cette bonne nouvelle du royaume sera pr&ecirc;ch&eacute;e dans le monde entier, pour servir de t&eacute;moignage &agrave; toutes les nations. Alors viendra la fin.</p>
	<!-- end bible --></div>
	Sa vision &eacute;tait et continue d&rsquo;&ecirc;tre l&rsquo;instauration du Royaume de Dieu parmi de milliers de groupes de personnes partout dans le monde, o&ugrave; Son nom sera sanctifi&eacute; et Sa volont&eacute; sera faite (<span class="popup-link" @click = "popUp('pop5')"> Matthieu 6 :9-10</span>; LSG).

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">9&nbsp;</sup>Voici donc comment vous devez prier: Notre P&egrave;re qui es aux cieux! Que ton nom soit sanctifi&eacute;;</p>

	<p><sup class="versenum">10&nbsp;</sup>que ton r&egrave;gne vienne; que ta volont&eacute; soit faite sur la terre comme au ciel.</p>
	<!-- end bible --></div>
	</li>
	<li class="nobreak-final-final">J&eacute;sus a montr&eacute; &agrave; Ses disciple comment se connecter aux hommes perdus, faire des disciples qui, &agrave; leur tour, feront &eacute;galement des disciples, et comment identifier et former des leaders qui iront r&eacute;p&eacute;ter ce processus dans tous les groupes de personnes. Depuis le ciel, J&eacute;sus a poursuivi ce qu&rsquo;Il a commenc&eacute; &agrave; faire pendant qu&rsquo;Il &eacute;tait sur la terre, &agrave; travers Ses disciples remplit de l&rsquo;Esprit selon Ses promesses: &laquo; En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les &oelig;uvres que je fais, et il en fera de plus grandes, parce que je m&rsquo;en vais au P&egrave;re &raquo; (<span class="popup-link" @click = "popUp('pop6')"> Jean 14 :12</span>; LSG) ;
	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les oeuvres que je fais, et il en fera de plus grandes, parce que je m&#39;en vais au P&egrave;re;</p>
	<!-- end bible --></div>
	&laquo; il vous est avantageux que je m&rsquo;en aille, car si je ne m&rsquo;en vais pas, le consolateur ne viendra pas vers vous &raquo; <span class="popup-link" @click = "popUp('pop7')"> (Jean 16:7</span>; LSG);

	<div class="popup invisible" id="pop7">&nbsp;</div>
	&laquo; &hellip; vous recevrez une puissance, le Saint-Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&rsquo;aux extr&eacute;mit&eacute;s de la terre. &raquo; (<span class="popup-link" @click = "popUp('pop8')"> Actes 1 :8</span>; LSG)

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>Mais vous recevrez une puissance, le Saint Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&#39;aux extr&eacute;mit&eacute;s de la terre.</p>
	<!-- end bible --></div>
	</li>
</ul>

<p>C&rsquo;est l&rsquo;histoire du livre des Actes. Cela nous montre le mouvement de l&rsquo;Esprit de Dieu qui &eacute;tablit et faire r&eacute;pandre le royaume &agrave; tous les hommes pendant que Ses disciples ont commenc&eacute; &agrave; vivre une vie d&eacute;pendante de l&rsquo;Esprit comme cela leur a &eacute;t&eacute; enseign&eacute;. Cela pr&eacute;sente &eacute;galement le contexte du mouvement qui nous aide &agrave; appliquer le reste des lettres du Nouveau Testament &agrave; la mission de j&eacute;sus. Pendant seulement une p&eacute;riode de 30 ann&eacute;es, une fondation &eacute;tait pos&eacute;e pour l&rsquo;expansion du royaume ; une fondation marqu&eacute;e par son impact sur la soci&eacute;t&eacute; et le d&eacute;veloppement de nouveaux disciples et de nouvelles &eacute;glises partout.</p>

<h2>P&eacute;riode 1: Les cons&eacute;quences de l&rsquo;explosion du Royaume en J&eacute;rusalem</h2>

<h2>[30-32 ap. J.-C.]</h2>

<p><strong>R&eacute;sum&eacute;:</strong> Cette p&eacute;riode couvre les premi&egrave;res ann&eacute;es apr&egrave;s la mort, la r&eacute;surrection et l&rsquo;ascension de J&eacute;sus. Les ap&ocirc;tres d&eacute;sign&eacute;s commencent &agrave; ob&eacute;ir &agrave; l&rsquo;ordre de faire des disciples mais ne sortaient pas de J&eacute;rusalem. La p&eacute;riode est marqu&eacute;e par une croissance explosive, la pers&eacute;cution, les miracles et les caract&eacute;ristiques fondamentales de la communaut&eacute; Chr&eacute;tienne<br />
&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Période 1: Les conséquences de l’explosion du Royaume en Jérusalem: ', '/content/M2/fra/multiply3/multiply3intro1.html')">
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