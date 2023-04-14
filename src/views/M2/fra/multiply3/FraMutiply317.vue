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
                        <div class="chapter_number ltr"><h1>17.</h1></div>
                        <div class="chapter_title ltr"><h1>Saul à Damas et Jérusalem</h1></div>
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
	<li>Lisez ou observez Actes 9:20-31 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 9:20-31</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">20&nbsp;</sup>Et aussit&ocirc;t il pr&ecirc;cha dans les synagogues que J&eacute;sus est le Fils de Dieu.</p>

<p><sup class="versenum">21&nbsp;</sup>Tous ceux qui l&#39;entendaient &eacute;taient dans l&#39;&eacute;tonnement, et disaient: N&#39;est-ce pas celui qui pers&eacute;cutait &agrave; J&eacute;rusalem ceux qui invoquent ce nom, et n&#39;est-il pas venu ici pour les emmener li&eacute;s devant les principaux sacrificateurs?</p>

<p><sup class="versenum">22&nbsp;</sup>Cependant Saul se fortifiait de plus en plus, et il confondait les Juifs qui habitaient Damas, d&eacute;montrant que J&eacute;sus est le Christ.</p>

<p><sup class="versenum">23&nbsp;</sup>Au bout d&#39;un certain temps, les Juifs se concert&egrave;rent pour le tuer,</p>

<p><sup class="versenum">24&nbsp;</sup>et leur complot parvint &agrave; la connaissance de Saul. On gardait les portes jour et nuit, afin de lui &ocirc;ter la vie.</p>

<p><sup class="versenum">25&nbsp;</sup>Mais, pendant une nuit, les disciples le prirent, et le descendirent par la muraille, dans une corbeille.</p>

<p><sup class="versenum">26&nbsp;</sup>Lorsqu&#39;il se rendit &agrave; J&eacute;rusalem, Saul t&acirc;cha de se joindre &agrave; eux; mais tous le craignaient, ne croyant pas qu&#39;il f&ucirc;t un disciple.</p>

<p><sup class="versenum">27&nbsp;</sup>Alors Barnabas, l&#39;ayant pris avec lui, le conduisit vers les ap&ocirc;tres, et leur raconta comment sur le chemin Saul avait vu le Seigneur, qui lui avait parl&eacute;, et comment &agrave; Damas il avait pr&ecirc;ch&eacute; franchement au nom de J&eacute;sus.</p>

<p><sup class="versenum">28&nbsp;</sup>Il allait et venait avec eux dans J&eacute;rusalem, et s&#39;exprimait en toute assurance au nom du Seigneur.</p>

<p><sup class="versenum">29&nbsp;</sup>Il parlait aussi et disputait avec les Hell&eacute;nistes; mais ceux-ci cherchaient &agrave; lui &ocirc;ter la vie.</p>

<p><sup class="versenum">30&nbsp;</sup>Les fr&egrave;res, l&#39;ayant su, l&#39;emmen&egrave;rent &agrave; C&eacute;sar&eacute;e, et le firent partir pour Tarse.</p>

<p><sup class="versenum">31&nbsp;</sup>L&#39;&Eacute;glise &eacute;tait en paix dans toute la Jud&eacute;e, la Galil&eacute;e et la Samarie, s&#39;&eacute;difiant et marchant dans la crainte du Seigneur, et elle s&#39;accroissait par l&#39;assistance du Saint Esprit.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/317.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 9:20-31&nbsp; </button>
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

<ul>
	<li class="nobreak-final-final">Les croyants de Damas &eacute;taient &eacute;tonn&eacute;s au sujet de Saul. Au lieu de les arr&ecirc;ter, Saul a commenc&eacute; par pr&ecirc;cher J&eacute;sus comme &eacute;tant &nbsp;le Fils vivant De Dieu. Les &eacute;tudes avanc&eacute;es de Saul lui ont permis d&rsquo;appliquer imm&eacute;diatement sa connaissance de l&rsquo;&Eacute;criture pour donner une preuve convaincante que J&eacute;sus &eacute;tait le Messie promis. J&eacute;sus a enseign&eacute; que les gens qui sont dot&eacute;s de telle connaissance &eacute;taient capables de ressortir des tr&eacute;sors de l&rsquo;Ancien Testament et de nouveaux enseignements sur le Royaume (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 13 :52</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">52&nbsp;</sup>Et il leur dit: C&#39;est pourquoi, tout scribe instruit de ce qui regarde le royaume des cieux est semblable &agrave; un ma&icirc;tre de maison qui tire de son tr&eacute;sor des choses nouvelles et des choses anciennes.</p>
	<!-- end bible --></div>
	Saul &eacute;tait si convaincant &nbsp;dans sa d&eacute;claration de t&eacute;moin que les Juifs ont du mal &agrave; trouver des arguments pour le conteste. Ils essayaient donc de le tuer &agrave; Damas. Quand Saul est venu en J&eacute;rusalem, seul Barnabas l&rsquo;a accept&eacute; et l&rsquo;a conduit vers les Ap&ocirc;tres. La vie de Saul &eacute;tait encore menac&eacute;e, donc les disciples le font partir, pour Tarse, sa ville natale dans la province de Cilicie situ&eacute;e &agrave; environ 930 km du Nord-Est de J&eacute;rusalem. Cette histoire comprend la deuxi&egrave;me d&eacute;claration sommaire trouv&eacute;e dans le livre des Actes : l&rsquo;&eacute;glise &eacute;tait en paix et s&rsquo;accroissait en nombre en marchant dans la crainte et la puissance de Dieu (<span class="popup-link" @click = "popUp('pop4')"> Actes 9 :31</span>).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">31&nbsp;</sup>L&#39;&Eacute;glise &eacute;tait en paix dans toute la Jud&eacute;e, la Galil&eacute;e et la Samarie, s&#39;&eacute;difiant et marchant dans la crainte du Seigneur, et elle s&#39;accroissait par l&#39;assistance du Saint Esprit.</p>
	<!-- end bible --></div>
	</li>
</ul>
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

			<td class="social" @click="share('lesson', 'Saul à Damas et Jérusalem: ', '/content/M2/fra/multiply3/mutiply317.html')">
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