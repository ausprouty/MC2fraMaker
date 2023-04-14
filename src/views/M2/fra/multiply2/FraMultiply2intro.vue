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
<h1>Être comme Jésus: le Modèle du Royaume</h1>
<div id="showVideoOptions"></div>
  <p>J&eacute;sus est notre mod&egrave;le de vie et de minist&egrave;re. Parce qu&rsquo;il est notre mod&egrave;le, il est important de connaitre son caract&egrave;re, ses priorit&eacute;s, et son processus de construction d&rsquo;un mouvement de formation de disciple. Ce mouvement se multiplie dans le but d&rsquo;accomplir la Grande Commission.</p>

<ul>
	<li class="nobreak-final-final">No&euml;l est le moment o&ugrave; nous c&eacute;l&eacute;brons le myst&egrave;re de la Parole (<span class="popup-link" @click = "popUp('pop1')"> Jean 1:1</span>).&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Au commencement &eacute;tait la Parole, et la Parole &eacute;tait avec Dieu, et la Parole &eacute;tait Dieu.</p>
	<!-- end bible --></div>
	La Parole est devenue pleinement humaine (<span class="popup-link" @click = "popUp('pop2')"> Jean 1:14</span>),&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Et la parole a &eacute;t&eacute; faite chair, et elle a habit&eacute; parmi nous, pleine de gr&acirc;ce et de v&eacute;rit&eacute;; et nous avons contempl&eacute; sa gloire, une gloire comme la gloire du Fils unique venu du P&egrave;re.</p>
	<!-- end bible --></div>
	n&eacute;e comme un gar&ccedil;on, J&eacute;sus de Nazareth. Il est venu de l&rsquo;&eacute;ternit&eacute; et est entr&eacute; dans le temps et l&rsquo;espace. Il est entr&eacute; dans une famille, une culture, un village, une tribu et a v&eacute;cu un jour &agrave; la fois dans l&#39;Isra&euml;l du premier si&egrave;cle sous la domination Romaine.</li>
</ul>

<p>Bien qu&#39;il soit pleinement Dieu, il a choisi de vivre sa vie comme un homme &agrave; part enti&egrave;re, dans une totale ob&eacute;issance &agrave; son P&egrave;re c&eacute;leste. Ce qu&#39;il a accompli dans sa vie et son minist&egrave;re, il l&#39;a accompli en tant qu&#39;homme de Nazareth, le Fils de l&#39;Homme, par la puissance et la pr&eacute;sence du Saint-Esprit en accomplissement de la volont&eacute; du P&egrave;re. Bien qu&#39;il ait eu le droit d&#39;agir &agrave; partir de sa divinit&eacute;, il a choisi de vivre uniquement &agrave; partir de sa parfaite humanit&eacute; sans p&eacute;ch&eacute; pour &ecirc;tre notre exemple dans la fa&ccedil;on de glorifier pleinement Dieu dans notre vie et dans notre minist&egrave;re. &nbsp;</p>

<ul>
	<li class="nobreak-final-final">J&eacute;sus &eacute;tait et sera toujours pleinement Dieu. M&ecirc;me s&#39;il avait toute l&#39;autorit&eacute;, le pouvoir et les ressources du Ciel &agrave; sa disposition, il ne s&#39;en est jamais servi. Il a plut&ocirc;t choisi de &laquo; devenir semblable &agrave; ses fr&egrave;res en tous points &raquo; (<span class="popup-link" @click = "popUp('pop3')"> H&eacute;breux 2:17</span>),&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">17&nbsp;</sup>En cons&eacute;quence, il a d&ucirc; &ecirc;tre rendu semblable en toutes choses &agrave; ses fr&egrave;res, afin qu&#39;il f&ucirc;t un souverain sacrificateur mis&eacute;ricordieux et fid&egrave;le dans le service de Dieu, pour faire l&#39;expiation des p&eacute;ch&eacute;s du peuple;</p>
	<!-- end bible --></div>
	mais sans p&eacute;ch&eacute;. Pour cette raison, le livre des H&eacute;breux nous encourage : &laquo; C&#39;est pourquoi, fr&egrave;res saints, qui participez &agrave; l&#39;appel c&eacute;leste, fixez vos pens&eacute;es sur J&eacute;sus, l&#39;ap&ocirc;tre et le grand pr&ecirc;tre que nous confessons &raquo;. (<span class="popup-link" @click = "popUp('pop4')"> H&eacute;breux 3:1</span>).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>C&#39;est pourquoi, fr&egrave;res saints, qui avez part &agrave; la vocation c&eacute;leste, consid&eacute;rez l&#39;ap&ocirc;tre et le souverain sacrificateur de la foi que nous professons,</p>
	<!-- end bible --></div>
	</li>
</ul>

<p>Les quatre r&eacute;dacteurs de l&#39;&Eacute;vangile font un r&eacute;sum&eacute; de sa vie et de ses enseignements. En &eacute;tudiant leur t&eacute;moignage &eacute;crit, nous pouvons en apprendre davantage sur le d&eacute;veloppement de son mouvement. Dans son humanit&eacute;, m&ecirc;me J&eacute;sus &eacute;tait soumis au temps et &agrave; l&#39;espace et vivait dans l&#39;ordre des heures, des jours, des semaines et des ann&eacute;es. Il a initi&eacute; et a d&eacute;velopp&eacute; son mouvement dans le temps. Par cons&eacute;quent, l&#39;&eacute;tude de cas de J&eacute;sus est tr&egrave;s instructive pour les Leaders. Nous pouvons comprendre comment sa vie et son mouvement se sont d&eacute;roul&eacute;s dans le temps en reconstituant une s&eacute;quence chronologique &agrave; partir des preuves fournies par les &eacute;vangiles.</p>

<ul>
	<li class="nobreak-final-final">Luc nous dit qu&#39;il a cherch&eacute; &agrave; fournir un &laquo; r&eacute;cit ordonn&eacute; &raquo; et bien document&eacute; de la vie de J&eacute;sus (<span class="popup-link" @click = "popUp('pop5')"> Luc 1:1-4</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Plusieurs ayant entrepris de composer un r&eacute;cit des &eacute;v&eacute;nements qui se sont accomplis parmi nous,</p>

	<p><sup class="versenum">2&nbsp;</sup>suivant ce que nous ont transmis ceux qui ont &eacute;t&eacute; des t&eacute;moins oculaires d&egrave;s le commencement et sont devenus des ministres de la parole,</p>

	<p><sup class="versenum">3&nbsp;</sup>il m&#39;a aussi sembl&eacute; bon, apr&egrave;s avoir fait des recherches exactes sur toutes ces choses depuis leur origine, de te les exposer par &eacute;crit d&#39;une mani&egrave;re suivie, excellent Th&eacute;ophile,</p>

	<p><sup class="versenum">4&nbsp;</sup>afin que tu reconnaisses la certitude des enseignements que tu as re&ccedil;us.</p>
	<!-- end bible --></div>
	Les autres &eacute;crivains ne se sont pas pr&eacute;occup&eacute;s de l&#39;ordre des &eacute;v&eacute;nements, mais ont organis&eacute; leurs r&eacute;cits autour de th&egrave;mes. Par exemple, Jean, le dernier des quatre &agrave; avoir &eacute;crit son &eacute;vangile, a enregistr&eacute; beaucoup de nouveaux &eacute;l&eacute;ments pour combler certaines lacunes dans le temps, en particulier les dix-huit premiers mois (Jean 1-4) et les derni&egrave;res semaines (Jean 12-21) de la vie et du minist&egrave;re terrestres de J&eacute;sus. En fait, Jean 13-20 ne couvre que trois jours !</li>
</ul>

<p>&nbsp;L&#39;&eacute;vangile de Luc nous donne quelques rep&egrave;res de date afin que nous puissions situer J&eacute;sus dans un contexte historique.</p>

<ul>
	<li class="nobreak-final-final"><em>Plusieurs ayant entrepris de composer un r&eacute;cit des &eacute;v&egrave;nements qui se sont accomplis parmi nous, suivant ce que nous ont transmis ceux qui ont &eacute;t&eacute; des t&eacute;moins oculaires d&egrave;s le commencement et sont devenus des ministres de la parole. Il m&rsquo;a aussi sembl&eacute; bon, apr&egrave;s avoir fait des recherches exactes sur toutes ces choses depuis leur origine, de te les exposer par &eacute;crit d&rsquo;une manie suivie, excellent Th&eacute;ophile, afin que tu reconnaisses la certitude des enseignements que tu as re&ccedil;us.</em> &ndash; <span class="popup-link" @click = "popUp('pop6')"> Luc 1:1-4</span>&nbsp;LSG.

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Plusieurs ayant entrepris de composer un r&eacute;cit des &eacute;v&eacute;nements qui se sont accomplis parmi nous,</p>

	<p><sup class="versenum">2&nbsp;</sup>suivant ce que nous ont transmis ceux qui ont &eacute;t&eacute; des t&eacute;moins oculaires d&egrave;s le commencement et sont devenus des ministres de la parole,</p>

	<p><sup class="versenum">3&nbsp;</sup>il m&#39;a aussi sembl&eacute; bon, apr&egrave;s avoir fait des recherches exactes sur toutes ces choses depuis leur origine, de te les exposer par &eacute;crit d&#39;une mani&egrave;re suivie, excellent Th&eacute;ophile,</p>

	<p><sup class="versenum">4&nbsp;</sup>afin que tu reconnaisses la certitude des enseignements que tu as re&ccedil;us.</p>
	<!-- end bible --></div>
	</li>
	<li class="nobreak-final-final">Luc nous dit que J&eacute;sus est n&eacute; pendant le r&egrave;gne du roi H&eacute;rode [le Grand] (Luc 1:5), pendant le r&egrave;gne de C&eacute;sar Auguste (<span class="popup-link" @click = "popUp('pop7')"> Luc 2:1-7</span>)&nbsp;
	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>En ce temps-l&agrave; parut un &eacute;dit de C&eacute;sar Auguste, ordonnant un recensement de toute la terre.</p>

	<p><sup class="versenum">2&nbsp;</sup>Ce premier recensement eut lieu pendant que Quirinius &eacute;tait gouverneur de Syrie.</p>

	<p><sup class="versenum">3&nbsp;</sup>Tous allaient se faire inscrire, chacun dans sa ville.</p>

	<p><sup class="versenum">4&nbsp;</sup>Joseph aussi monta de la Galil&eacute;e, de la ville de Nazareth, pour se rendre en Jud&eacute;e, dans la ville de David, appel&eacute;e Bethl&eacute;hem, parce qu&#39;il &eacute;tait de la maison et de la famille de David,</p>

	<p><sup class="versenum">5&nbsp;</sup>afin de se faire inscrire avec Marie, sa fianc&eacute;e, qui &eacute;tait enceinte.</p>

	<p><sup class="versenum">6&nbsp;</sup>Pendant qu&#39;ils &eacute;taient l&agrave;, le temps o&ugrave; Marie devait accoucher arriva,</p>

	<p><sup class="versenum">7&nbsp;</sup>et elle enfanta son fils premier-n&eacute;. Elle l&#39;emmaillota, et le coucha dans une cr&egrave;che, parce qu&#39;il n&#39;y avait pas de place pour eux dans l&#39;h&ocirc;tellerie.</p>
	<!-- end bible --></div>
	et pendant que Quirinius &eacute;tait gouverneur de Syrie (<span class="popup-link" @click = "popUp('pop8')"> Luc 2:2</span>).&nbsp;

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">2&nbsp;</sup>Ce premier recensement eut lieu pendant que Quirinius &eacute;tait gouverneur de Syrie.</p>
	<!-- end bible --></div>
	&nbsp;Il d&eacute;clare &eacute;galement que J&eacute;sus a commenc&eacute; son minist&egrave;re pendant le 15&egrave;me r&egrave;gne de Tib&egrave;re C&eacute;sar (<span class="popup-link" @click = "popUp('pop9')"> Luc 3:1-2</span>)

	<div class="popup invisible" id="pop9"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>La quinzi&egrave;me ann&eacute;e du r&egrave;gne de Tib&egrave;re C&eacute;sar, -lorsque Ponce Pilate &eacute;tait gouverneur de la Jud&eacute;e, H&eacute;rode t&eacute;trarque de la Galil&eacute;e, son fr&egrave;re Philippe t&eacute;trarque de l&#39;Itur&eacute;e et du territoire de la Trachonite, Lysanias t&eacute;trarque de l&#39;Abil&egrave;ne,</p>

	<p><sup class="versenum">2&nbsp;</sup>et du temps des souverains sacrificateurs Anne et Ca&iuml;phe, -la parole de Dieu fut adress&eacute;e &agrave; Jean, fils de Zacharie, dans le d&eacute;sert.</p>
	<!-- end bible --></div>
	et que J&eacute;sus avait environ 30 ans lorsqu&#39;il a commenc&eacute; (<span class="popup-link" @click = "popUp('pop10')"> Luc 3:21-23</span>).

	<div class="popup invisible" id="pop10"><!-- begin bible -->
	<p><sup class="versenum">21&nbsp;</sup>Tout le peuple se faisant baptiser, J&eacute;sus fut aussi baptis&eacute;; et, pendant qu&#39;il priait, le ciel s&#39;ouvrit,</p>

	<p><sup class="versenum">22&nbsp;</sup>et le Saint Esprit descendit sur lui sous une forme corporelle, comme une colombe. Et une voix fit entendre du ciel ces paroles: Tu es mon Fils bien-aim&eacute;; en toi j&#39;ai mis toute mon affection.</p>

	<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus avait environ trente ans lorsqu&#39;il commen&ccedil;a son minist&egrave;re, &eacute;tant, comme on le croyait, fils de Joseph, fils d&#39;H&eacute;li,</p>
	<!-- end bible --></div>
	C&#39;est important car cela nous aide &agrave; mieux comprendre quand et pendant combien de temps J&eacute;sus a exerc&eacute; son minist&egrave;re. Nous pouvons commencer &agrave; voir les mesures qu&#39;il a prises pour jeter les bases de la formation de disciples, faire de ses disciples des faiseurs de disciples et, avec le temps, &eacute;quiper les faiseurs de disciples &eacute;prouv&eacute;s pour qu&#39;ils deviennent des leaders de Mouvements Multipli&eacute;s.</li>
</ul>

<p>Les s&eacute;ries de podcasts et de vid&eacute;os sont disponibles &agrave; l&#39;adresse suivante : https://vimeo.com/channels/movementbuilding &nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Être comme Jésus: le Modèle du Royaume: ', '/content/M2/fra/multiply2/multiply2intro.html')">
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