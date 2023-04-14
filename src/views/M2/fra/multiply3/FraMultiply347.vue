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
                        <div class="chapter_number ltr"><h1>47.</h1></div>
                        <div class="chapter_title ltr"><h1>Complot pour tuer Paul</h1></div>
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
	<li>Lisez ou observez Actes 23:12-35 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 23:12-35</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>Quand le jour fut venu, les Juifs form&egrave;rent un complot, et firent des impr&eacute;cations contre eux-m&ecirc;mes, en disant qu&#39;ils s&#39;abstiendraient de manger et de boire jusqu&#39;&agrave; ce qu&#39;ils eussent tu&eacute; Paul.</p>

<p><sup class="versenum">13&nbsp;</sup>Ceux qui form&egrave;rent ce complot &eacute;taient plus de quarante,</p>

<p><sup class="versenum">14&nbsp;</sup>et ils all&egrave;rent trouver les principaux sacrificateurs et les anciens, auxquels ils dirent: Nous nous sommes engag&eacute;s, avec des impr&eacute;cations contre nous-m&ecirc;mes, &agrave; ne rien manger jusqu&#39;&agrave; ce que nous ayons tu&eacute; Paul.</p>

<p><sup class="versenum">15&nbsp;</sup>Vous donc, maintenant, adressez-vous avec le sanh&eacute;drin au tribun, pour qu&#39;il l&#39;am&egrave;ne devant vous, comme si vous vouliez examiner sa cause plus exactement; et nous, avant qu&#39;il approche, nous sommes pr&ecirc;ts &agrave; le tuer.</p>

<p><sup class="versenum">16&nbsp;</sup>Le fils de la soeur de Paul, ayant eu connaissance du guet-apens, alla dans la forteresse en informer Paul.</p>

<p><sup class="versenum">17&nbsp;</sup>Paul appela l&#39;un des centeniers, et dit: M&egrave;ne ce jeune homme vers le tribun, car il a quelque chose &agrave; lui rapporter.</p>

<p><sup class="versenum">18&nbsp;</sup>Le centenier prit le jeune homme avec lui, le conduisit vers le tribun, et dit: Le prisonnier Paul m&#39;a appel&eacute;, et il m&#39;a pri&eacute; de t&#39;amener ce jeune homme, qui a quelque chose &agrave; te dire.</p>

<p><sup class="versenum">19&nbsp;</sup>Le tribun, prenant le jeune homme par la main, et se retirant &agrave; l&#39;&eacute;cart, lui demanda: Qu&#39;as-tu &agrave; m&#39;annoncer?</p>

<p><sup class="versenum">20&nbsp;</sup>Il r&eacute;pondit: Les Juifs sont convenus de te prier d&#39;amener Paul demain devant le sanh&eacute;drin, comme si tu devais t&#39;enqu&eacute;rir de lui plus exactement.</p>

<p><sup class="versenum">21&nbsp;</sup>Ne les &eacute;coute pas, car plus de quarante d&#39;entre eux lui dressent un guet-apens, et se sont engag&eacute;s, avec des impr&eacute;cations contre eux-m&ecirc;mes, &agrave; ne rien manger ni boire jusqu&#39;&agrave; ce qu&#39;ils l&#39;aient tu&eacute;; maintenant ils sont pr&ecirc;ts, et n&#39;attendent que ton consentement.</p>

<p><sup class="versenum">22&nbsp;</sup>Le tribun renvoya le jeune homme, apr&egrave;s lui avoir recommand&eacute; de ne parler &agrave; personne de ce rapport qu&#39;il lui avait fait.</p>

<p><sup class="versenum">23&nbsp;</sup>Ensuite il appela deux des centeniers, et dit: Tenez pr&ecirc;ts, d&egrave;s la troisi&egrave;me heure de la nuit, deux cents soldats, soixante-dix cavaliers et deux cents archers, pour aller jusqu&#39;&agrave; C&eacute;sar&eacute;e.</p>

<p><sup class="versenum">24&nbsp;</sup>Qu&#39;il y ait aussi des montures pour Paul, afin qu&#39;on le m&egrave;ne sain et sauf au gouverneur F&eacute;lix.</p>

<p><sup class="versenum">25&nbsp;</sup>Il &eacute;crivit une lettre ainsi con&ccedil;ue:</p>

<p><sup class="versenum">26&nbsp;</sup>Claude Lysias au tr&egrave;s excellent gouverneur F&eacute;lix, salut!</p>

<p><sup class="versenum">27&nbsp;</sup>Cet homme, dont les Juifs s&#39;&eacute;taient saisis, allait &ecirc;tre tu&eacute; par eux, lorsque je survins avec des soldats et le leur enlevai, ayant appris qu&#39;il &eacute;tait Romain.</p>

<p><sup class="versenum">28&nbsp;</sup>Voulant conna&icirc;tre le motif pour lequel ils l&#39;accusaient, je l&#39;amenai devant leur sanh&eacute;drin.</p>

<p><sup class="versenum">29&nbsp;</sup>J&#39;ai trouv&eacute; qu&#39;il &eacute;tait accus&eacute; au sujet de questions relatives &agrave; leur loi, mais qu&#39;il n&#39;avait commis aucun crime qui m&eacute;rite la mort ou la prison.</p>

<p><sup class="versenum">30&nbsp;</sup>Inform&eacute; que les Juifs lui dressaient des emb&ucirc;ches, je te l&#39;ai aussit&ocirc;t envoy&eacute;, en faisant savoir &agrave; ses accusateurs qu&#39;ils eussent &agrave; s&#39;adresser eux-m&ecirc;mes &agrave; toi. Adieu.</p>

<p><sup class="versenum">31&nbsp;</sup>Les soldats, selon l&#39;ordre qu&#39;ils avaient re&ccedil;u, prirent Paul, et le conduisirent pendant la nuit jusqu&#39;&agrave; Antipatris.</p>

<p><sup class="versenum">32&nbsp;</sup>Le lendemain, laissant les cavaliers poursuivre la route avec lui, ils retourn&egrave;rent &agrave; la forteresse.</p>

<p><sup class="versenum">33&nbsp;</sup>Arriv&eacute;s &agrave; C&eacute;sar&eacute;e, les cavaliers remirent la lettre au gouverneur, et lui pr&eacute;sent&egrave;rent Paul.</p>

<p><sup class="versenum">34&nbsp;</sup>Le gouverneur, apr&egrave;s avoir lu la lettre, demanda de quelle province &eacute;tait Paul. Ayant appris qu&#39;il &eacute;tait de la Cilicie:</p>

<p><sup class="versenum">35&nbsp;</sup>Je t&#39;entendrai, dit-il, quand tes accusateurs seront venus. Et il ordonna qu&#39;on le gard&acirc;t dans le pr&eacute;toire d&#39;H&eacute;rode.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/347.mp4" type="button" class="external-movie">
         Regardez Actes 23:12-35 </button>
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
	<li class="nobreak-final-final">Pendant toute la vie chr&eacute;tienne de Paul, les Juifs qui ont rejet&eacute; J&eacute;sus l&#39;ont &eacute;galement rejet&eacute; ainsi que l&#39;&Eacute;vangile. Nous nous souvenons de l&rsquo;enseignement de J&eacute;sus: &laquo;celui qui vous rejette me rejette ; et celui qui me rejette, rejette celui qui m&rsquo;a envoy&eacute;&raquo; (<span class="popup-link" @click = "popUp('pop3')"> Luc 10:16</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Celui qui vous &eacute;coute m&#39;&eacute;coute, et celui qui vous rejette me rejette; et celui qui me rejette rejette celui qui m&#39;a envoy&eacute;.</p>
	<!-- end bible --></div>
	Les Juifs consid&eacute;raient Paul comme un blasph&eacute;mateur et son message comme une menace pour leur propre vision nationaliste &eacute;go&iuml;ste du dessein de Dieu. Nous voyons la souverainet&eacute; de Dieu qui a utilis&eacute; le neveu de Paul pour r&eacute;v&eacute;ler le complot visant &agrave; le faire assassiner. En r&eacute;ponse, le tribun a envoy&eacute; 470 soldats romains pour transporter Paul en toute s&eacute;curit&eacute; sur les 112 km jusqu&#39;&agrave; la ville baln&eacute;aire de C&eacute;sar&eacute;e. Le gouverneur F&eacute;lix le mit sous garde dans le pr&eacute;toire d&#39;&eacute;t&eacute; de l&#39;ancien roi H&eacute;rode le Grand (<span class="popup-link" @click = "popUp('pop4')"> Matthieu 2: 1</span>;&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>J&eacute;sus &eacute;tant n&eacute; &agrave; Bethl&eacute;hem en Jud&eacute;e, au temps du roi H&eacute;rode, voici des mages d&#39;Orient arriv&egrave;rent &agrave; J&eacute;rusalem,</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop5')"> Luc 1: 5</span>).&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">5&nbsp;</sup>Du temps d&#39;H&eacute;rode, roi de Jud&eacute;e, il y avait un sacrificateur, nomm&eacute; Zacharie, de la classe d&#39;Abia; sa femme &eacute;tait d&#39;entre les filles d&#39;Aaron, et s&#39;appelait &Eacute;lisabeth.</p>
	<!-- end bible --></div>
	Cet exemple tir&eacute; de la vie de Paul nous montre que le Seigneur est avec ceux qui poursuivent le dessein de son Royaume et que l&rsquo;endroit le plus s&ucirc;r se trouve dans la volont&eacute; du P&egrave;re.</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Complot pour tuer Paul: ', '/content/M2/fra/multiply3/multiply347.html')">
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