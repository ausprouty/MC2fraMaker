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
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>15.</h1></div>
                        <div class="chapter_title ltr"><h1>L'Esprit conduit Philippe vers une personne de paix stratégique</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 8:26-40 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 8:26-40</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">26&nbsp;</sup>Un ange du Seigneur, s&#39;adressant &agrave; Philippe, lui dit: L&egrave;ve-toi, et va du c&ocirc;t&eacute; du midi, sur le chemin qui descend de J&eacute;rusalem &agrave; Gaza, celui qui est d&eacute;sert.</p>

<p><sup class="versenum">27&nbsp;</sup>Il se leva, et partit. Et voici, un &Eacute;thiopien, un eunuque, ministre de Candace, reine d&#39;&Eacute;thiopie, et surintendant de tous ses tr&eacute;sors, venu &agrave; J&eacute;rusalem pour adorer,</p>

<p><sup class="versenum">28&nbsp;</sup>s&#39;en retournait, assis sur son char, et lisait le proph&egrave;te &Eacute;sa&iuml;e.</p>

<p><sup class="versenum">29&nbsp;</sup>L&#39;Esprit dit &agrave; Philippe: Avance, et approche-toi de ce char.</p>

<p><sup class="versenum">30&nbsp;</sup>Philippe accourut, et entendit l&#39;&Eacute;thiopien qui lisait le proph&egrave;te &Eacute;sa&iuml;e. Il lui dit: Comprends-tu ce que tu lis?</p>

<p><sup class="versenum">31&nbsp;</sup>Il r&eacute;pondit: Comment le pourrais-je, si quelqu&#39;un ne me guide? Et il invita Philippe &agrave; monter et &agrave; s&#39;asseoir avec lui.</p>

<p><sup class="versenum">32&nbsp;</sup>Le passage de l&#39;&Eacute;criture qu&#39;il lisait &eacute;tait celui-ci: Il a &eacute;t&eacute; men&eacute; comme une brebis &agrave; la boucherie; Et, comme un agneau muet devant celui qui le tond, Il n&#39;a point ouvert la bouche.</p>

<p><sup class="versenum">33&nbsp;</sup>Dans son humiliation, son jugement a &eacute;t&eacute; lev&eacute;. Et sa post&eacute;rit&eacute;, qui la d&eacute;peindra? Car sa vie a &eacute;t&eacute; retranch&eacute;e de la terre.</p>

<p><sup class="versenum">34&nbsp;</sup>L&#39;eunuque dit &agrave; Philippe: Je te prie, de qui le proph&egrave;te parle-t-il ainsi? Est-ce de lui-m&ecirc;me, ou de quelque autre?</p>

<p><sup class="versenum">35&nbsp;</sup>Alors Philippe, ouvrant la bouche et commen&ccedil;ant par ce passage, lui annon&ccedil;a la bonne nouvelle de J&eacute;sus.</p>

<p><sup class="versenum">36&nbsp;</sup>Comme ils continuaient leur chemin, ils rencontr&egrave;rent de l&#39;eau. Et l&#39;eunuque dit: Voici de l&#39;eau; qu&#39;est-ce qui emp&ecirc;che que je ne sois baptis&eacute;?</p>

<p><sup class="versenum">37&nbsp;</sup>Philippe dit: Si tu crois de tout ton coeur, cela est possible. L&#39;eunuque r&eacute;pondit: Je crois que J&eacute;sus Christ est le Fils de Dieu.</p>

<p><sup class="versenum">38&nbsp;</sup>Il fit arr&ecirc;ter le char; Philippe et l&#39;eunuque descendirent tous deux dans l&#39;eau, et Philippe baptisa l&#39;eunuque.</p>

<p><sup class="versenum">39&nbsp;</sup>Quand ils furent sortis de l&#39;eau, l&#39;Esprit du Seigneur enleva Philippe, et l&#39;eunuque ne le vit plus. Tandis que, joyeux, il poursuivait sa route,</p>

<p><sup class="versenum">40&nbsp;</sup>Philippe se trouva dans Azot, d&#39;o&ugrave; il alla jusqu&#39;&agrave; C&eacute;sar&eacute;e, en &eacute;vang&eacute;lisant toutes les villes par lesquelles il passait.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/315.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 8:26-40&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>L&rsquo;Esprit a interrompu le minist&egrave;re fructueux de Philippe dans la Samarie en l&rsquo;envoyant dans un endroit au sud d&rsquo;Isra&euml;l pour rencontrer une personne de paix strat&eacute;gique. Philippe a montr&eacute; son c&oelig;ur ob&eacute;issant et une sensibilit&eacute; &agrave; l&rsquo;Esprit en allant sans connaitre les d&eacute;tails de pourquoi il a &eacute;t&eacute; envoy&eacute;. Le leader &Eacute;thiopien qu&rsquo;il a rencontr&eacute; &eacute;tait un homme non-Juif qui avait accept&eacute; la foi des Juifs. En tant qu&rsquo;une personne non-juive et un eunuque (quelqu&rsquo;un qui avait &eacute;t&eacute; consacr&eacute; &agrave; servir dans une cour f&eacute;minine), il ne serait &nbsp;pas pleinement accept&eacute; dans la foi par les Juifs. Mais J&eacute;sus &eacute;tait pr&ecirc;t &agrave; l&rsquo;accepter ! le Seigneur aurait pr&eacute;par&eacute; le c&oelig;ur de l&rsquo;&Eacute;thiopien et a utilis&eacute; Philippe pour lui annoncer la Bonne Nouvelle. Philippe a suivi le m&ecirc;me mod&egrave;le de bapt&ecirc;me qu&rsquo;il a appris pendant qu&rsquo;il &eacute;tait en J&eacute;rusalem et l&rsquo;a utilis&eacute; aussi en Samarie. L&rsquo;&Eacute;thiopien a cru et a &eacute;t&eacute; en m&ecirc;me temps baptis&eacute;. Philippe annon&ccedil;ait l&rsquo;&eacute;vangile dans toutes les villes tout long de la c&ocirc;te d&rsquo;Isra&euml;l. Il s&rsquo;est finalement install&eacute; &agrave; C&eacute;sar&eacute;e, qui &eacute;tait un grand port international de la ville d&rsquo;Isra&euml;l et le si&egrave;ge de la puissance Romaine dans la province.</p>

<p>&nbsp;</p>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
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

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'L\'Esprit conduit Philippe vers une personne de paix stratégique: ', '/content/M2/fra/multiply3/mutiply315.html')">
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