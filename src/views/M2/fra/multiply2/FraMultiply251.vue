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
                        <div class="chapter_number ltr"><h1>51.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership Berger</h1></div>
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
	<li>Lisez ou observez Jean 21:1-25 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 21</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s cela, J&eacute;sus se montra encore aux disciples, sur les bords de la mer de Tib&eacute;riade. Et voici de quelle mani&egrave;re il se montra.</p>

<p><sup class="versenum">2&nbsp;</sup>Simon Pierre, Thomas, appel&eacute; Didyme, Nathana&euml;l, de Cana en Galil&eacute;e, les fils de Z&eacute;b&eacute;d&eacute;e, et deux autres disciples de J&eacute;sus, &eacute;taient ensemble.</p>

<p><sup class="versenum">3&nbsp;</sup>Simon Pierre leur dit: Je vais p&ecirc;cher. Ils lui dirent: Nous allons aussi avec toi. Ils sortirent et mont&egrave;rent dans une barque, et cette nuit-l&agrave; ils ne prirent rien.</p>

<p><sup class="versenum">4&nbsp;</sup>Le matin &eacute;tant venu, J&eacute;sus se trouva sur le rivage; mais les disciples ne savaient pas que c&#39;&eacute;tait J&eacute;sus.</p>

<p><sup class="versenum">5&nbsp;</sup>J&eacute;sus leur dit: Enfants, n&#39;avez-vous rien &agrave; manger? Ils lui r&eacute;pondirent: Non.</p>

<p><sup class="versenum">6&nbsp;</sup>Il leur dit: Jetez le filet du c&ocirc;t&eacute; droit de la barque, et vous trouverez. Ils le jet&egrave;rent donc, et ils ne pouvaient plus le retirer, &agrave; cause de la grande quantit&eacute; de poissons.</p>

<p><sup class="versenum">7&nbsp;</sup>Alors le disciple que J&eacute;sus aimait dit &agrave; Pierre: C&#39;est le Seigneur! Et Simon Pierre, d&egrave;s qu&#39;il eut entendu que c&#39;&eacute;tait le Seigneur, mit son v&ecirc;tement et sa ceinture, car il &eacute;tait nu, et se jeta dans la mer.</p>

<p><sup class="versenum">8&nbsp;</sup>Les autres disciples vinrent avec la barque, tirant le filet plein de poissons, car ils n&#39;&eacute;taient &eacute;loign&eacute;s de terre que d&#39;environ deux cents coud&eacute;es.</p>

<p><sup class="versenum">9&nbsp;</sup>Lorsqu&#39;ils furent descendus &agrave; terre, ils virent l&agrave; des charbons allum&eacute;s, du poisson dessus, et du pain.</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus leur dit: Apportez des poissons que vous venez de prendre.</p>

<p><sup class="versenum">11&nbsp;</sup>Simon Pierre monta dans la barque, et tira &agrave; terre le filet plein de cent cinquante-trois grands poissons; et quoiqu&#39;il y en e&ucirc;t tant, le filet ne se rompit point.</p>

<p><sup class="versenum">12&nbsp;</sup>J&eacute;sus leur dit: Venez, mangez. Et aucun des disciples n&#39;osait lui demander: Qui es-tu? sachant que c&#39;&eacute;tait le Seigneur.</p>

<p><sup class="versenum">13&nbsp;</sup>J&eacute;sus s&#39;approcha, prit le pain, et leur en donna; il fit de m&ecirc;me du poisson.</p>

<p><sup class="versenum">14&nbsp;</sup>C&#39;&eacute;tait d&eacute;j&agrave; la troisi&egrave;me fois que J&eacute;sus se montrait &agrave; ses disciples depuis qu&#39;il &eacute;tait ressuscit&eacute; des morts.</p>

<p><sup class="versenum">15&nbsp;</sup>Apr&egrave;s qu&#39;ils eurent mang&eacute;, J&eacute;sus dit &agrave; Simon Pierre: Simon, fils de Jonas, m&#39;aimes-tu plus que ne m&#39;aiment ceux-ci? Il lui r&eacute;pondit: Oui, Seigneur, tu sais que je t&#39;aime. J&eacute;sus lui dit: Pais mes agneaux.</p>

<p><sup class="versenum">16&nbsp;</sup>Il lui dit une seconde fois: Simon, fils de Jonas, m&#39;aimes-tu? Pierre lui r&eacute;pondit: Oui, Seigneur, tu sais que je t&#39;aime. J&eacute;sus lui dit: Pais mes brebis.</p>

<p><sup class="versenum">17&nbsp;</sup>Il lui dit pour la troisi&egrave;me fois: Simon, fils de Jonas, m&#39;aimes-tu? Pierre fut attrist&eacute; de ce qu&#39;il lui avait dit pour la troisi&egrave;me fois: M&#39;aimes-tu? Et il lui r&eacute;pondit: Seigneur, tu sais toutes choses, tu sais que je t&#39;aime. J&eacute;sus lui dit: Pais mes brebis.</p>

<p><sup class="versenum">18&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je te le dis, quand tu &eacute;tais plus jeune, tu te ceignais toi-m&ecirc;me, et tu allais o&ugrave; tu voulais; mais quand tu seras vieux, tu &eacute;tendras tes mains, et un autre te ceindra, et te m&egrave;nera o&ugrave; tu ne voudras pas.</p>

<p><sup class="versenum">19&nbsp;</sup>Il dit cela pour indiquer par quelle mort Pierre glorifierait Dieu. Et ayant ainsi parl&eacute;, il lui dit: Suis-moi.</p>

<p><sup class="versenum">20&nbsp;</sup>Pierre, s&#39;&eacute;tant retourn&eacute;, vit venir apr&egrave;s eux le disciple que J&eacute;sus aimait, celui qui, pendant le souper, s&#39;&eacute;tait pench&eacute; sur la poitrine de J&eacute;sus, et avait dit: Seigneur, qui est celui qui te livre?</p>

<p><sup class="versenum">21&nbsp;</sup>En le voyant, Pierre dit &agrave; J&eacute;sus: Et celui-ci, Seigneur, que lui arrivera-t-il?</p>

<p><sup class="versenum">22&nbsp;</sup>J&eacute;sus lui dit: Si je veux qu&#39;il demeure jusqu&#39;&agrave; ce que je vienne, que t&#39;importe? Toi, suis-moi.</p>

<p><sup class="versenum">23&nbsp;</sup>L&agrave;-dessus, le bruit courut parmi les fr&egrave;res que ce disciple ne mourrait point. Cependant J&eacute;sus n&#39;avait pas dit &agrave; Pierre qu&#39;il ne mourrait point; mais: Si je veux qu&#39;il demeure jusqu&#39;&agrave; ce que je vienne, que t&#39;importe?</p>

<p><sup class="versenum">24&nbsp;</sup>C&#39;est ce disciple qui rend t&eacute;moignage de ces choses, et qui les a &eacute;crites. Et nous savons que son t&eacute;moignage est vrai.</p>

<p><sup class="versenum">25&nbsp;</sup>J&eacute;sus a fait encore beaucoup d&#39;autres choses; si on les &eacute;crivait en d&eacute;tail, je ne pense pas que le monde m&ecirc;me p&ucirc;t contenir les livres qu&#39;on &eacute;crirait.</p>

<p>&nbsp;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/251.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 21:1-25&nbsp; </button>
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

<p>Apr&egrave;s &ecirc;tre ressuscit&eacute; des morts, J&eacute;sus appara&icirc;t &agrave; ses disciples &agrave; plusieurs reprises. Jusqu&#39;&agrave; 500 personnes l&rsquo;ont vu. A une de ces occasions, en Galil&eacute;e, il rend visite &agrave; Ses leaders qui sont retourn&eacute;s &agrave; leur ancienne vie de p&ecirc;che. Ils se sont rappeler l&rsquo;occasion pr&eacute;c&eacute;dente o&ugrave; ils ont p&ecirc;ch&eacute; toute la nuit et n&#39;ont rien attrap&eacute;. Quand ils ont exp&eacute;riment&eacute; le m&ecirc;me type de miracle de fourniture de poisson comme ils l&#39;ont eu quelques ann&eacute;es auparavant, ils reconnaissent que c&#39;&eacute;tait J&eacute;sus. Pierre &eacute;tait ravi de revoir le Seigneur. J&eacute;sus a parl&eacute; avec lui de son engagement du fond de son c&oelig;ur. Il a demand&eacute; si Pierre l&#39;aime plus que son ancien mode de vie. Si c&#39;est le cas, alors il devrait se pr&eacute;occuper des choses dont J&eacute;sus se soucie. Il devrait prendre soin des autres comme J&eacute;sus l&#39;a fait pour lui. Une fois de plus, Pierre fut restaur&eacute; et appel&eacute; &agrave; suivre J&eacute;sus et continuer le travail de p&ecirc;che et de soin des hommes. C&#39;est la derni&egrave;re fois que nous voyons Pierre retourner &agrave; la p&ecirc;che.</p>

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

			<td class="social" @click="share('lesson', 'Leadership Berger: ', '/content/M2/fra/multiply2/multiply251.html')">
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