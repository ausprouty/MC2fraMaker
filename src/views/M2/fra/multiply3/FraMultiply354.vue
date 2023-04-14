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
                        <div class="chapter_number ltr"><h1>54.</h1></div>
                        <div class="chapter_title ltr"><h1>Ministère en étant dans une maison d'arrêt à Rome</h1></div>
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
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
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
	<li>Expliquez que la vie de Christ est divis&eacute;e en 5 p&eacute;riodes: Pr&eacute;paration, fondements du minist&egrave;re, formation pour le minist&egrave;re, &eacute;vang&eacute;lisation explosif, Multiplication du leadership</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 28:11-31 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 28:11-31</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">11&nbsp;</sup>Apr&egrave;s un s&eacute;jour de trois mois, nous nous embarqu&acirc;mes sur un navire d&#39;Alexandrie, qui avait pass&eacute; l&#39;hiver dans l&#39;&icirc;le, et qui portait pour enseigne les Dioscures.</p>

<p><sup class="versenum">12&nbsp;</sup>Ayant abord&eacute; &agrave; Syracuse, nous y rest&acirc;mes trois jours.</p>

<p><sup class="versenum">13&nbsp;</sup>De l&agrave;, en suivant la c&ocirc;te, nous atteign&icirc;mes Reggio; et, le vent du midi s&#39;&eacute;tant lev&eacute; le lendemain, nous f&icirc;mes en deux jours le trajet jusqu&#39;&agrave; Pouzzoles,</p>

<p><sup class="versenum">14&nbsp;</sup>o&ugrave; nous trouv&acirc;mes des fr&egrave;res qui nous pri&egrave;rent de passer sept jours avec eux. Et c&#39;est ainsi que nous all&acirc;mes &agrave; Rome.</p>

<p><sup class="versenum">15&nbsp;</sup>De Rome vinrent &agrave; notre rencontre, jusqu&#39;au Forum d&#39;Appius et aux Trois Tavernes, les fr&egrave;res qui avaient entendu parler de nous. Paul, en les voyant, rendit gr&acirc;ces &agrave; Dieu, et prit courage.</p>

<p><sup class="versenum">16&nbsp;</sup>Lorsque nous f&ucirc;mes arriv&eacute;s &agrave; Rome, on permit &agrave; Paul de demeurer en son particulier, avec un soldat qui le gardait.</p>

<p><sup class="versenum">17&nbsp;</sup>Au bout de trois jours, Paul convoqua les principaux des Juifs; et, quand ils furent r&eacute;unis, il leur adressa ces paroles: Hommes fr&egrave;res, sans avoir rien fait contre le peuple ni contre les coutumes de nos p&egrave;res, j&#39;ai &eacute;t&eacute; mis en prison &agrave; J&eacute;rusalem et livr&eacute; de l&agrave; entre les mains des Romains.</p>

<p><sup class="versenum">18&nbsp;</sup>Apr&egrave;s m&#39;avoir interrog&eacute;, ils voulaient me rel&acirc;cher, parce qu&#39;il n&#39;y avait en moi rien qui m&eacute;rit&acirc;t la mort.</p>

<p><sup class="versenum">19&nbsp;</sup>Mais les Juifs s&#39;y oppos&egrave;rent, et j&#39;ai &eacute;t&eacute; forc&eacute; d&#39;en appeler &agrave; C&eacute;sar, n&#39;ayant du reste aucun dessein d&#39;accuser ma nation.</p>

<p><sup class="versenum">20&nbsp;</sup>Voil&agrave; pourquoi j&#39;ai demand&eacute; &agrave; vous voir et &agrave; vous parler; car c&#39;est &agrave; cause de l&#39;esp&eacute;rance d&#39;Isra&euml;l que je porte cette cha&icirc;ne.</p>

<p><sup class="versenum">21&nbsp;</sup>Ils lui r&eacute;pondirent: Nous n&#39;avons re&ccedil;u de Jud&eacute;e aucune lettre &agrave; ton sujet, et il n&#39;est venu aucun fr&egrave;re qui ait rapport&eacute; ou dit du mal de toi.</p>

<p><sup class="versenum">22&nbsp;</sup>Mais nous voudrions apprendre de toi ce que tu penses, car nous savons que cette secte rencontre partout de l&#39;opposition.</p>

<p><sup class="versenum">23&nbsp;</sup>Ils lui fix&egrave;rent un jour, et plusieurs vinrent le trouver dans son logis. Paul leur annon&ccedil;a le royaume de Dieu, en rendant t&eacute;moignage, et en cherchant, par la loi de Mo&iuml;se et par les proph&egrave;tes, &agrave; les persuader de ce qui concerne J&eacute;sus. L&#39;entretien dura depuis le matin jusqu&#39;au soir.</p>

<p><sup class="versenum">24&nbsp;</sup>Les uns furent persuad&eacute;s par ce qu&#39;il disait, et les autres ne crurent point.</p>

<p><sup class="versenum">25&nbsp;</sup>Comme ils se retiraient en d&eacute;saccord, Paul n&#39;ajouta que ces mots: C&#39;est avec raison que le Saint Esprit, parlant &agrave; vos p&egrave;res par le proph&egrave;te &Eacute;sa&iuml;e, a dit:</p>

<p><sup class="versenum">26&nbsp;</sup>Va vers ce peuple, et dis: Vous entendrez de vos oreilles, et vous ne comprendrez point; Vous regarderez de vos yeux, et vous ne verrez point.</p>

<p><sup class="versenum">27&nbsp;</sup>Car le coeur de ce peuple est devenu insensible; Ils ont endurci leurs oreilles, et ils ont ferm&eacute; leurs yeux, De peur qu&#39;ils ne voient de leurs yeux, qu&#39;ils n&#39;entendent de leurs oreilles, Qu&#39;ils ne comprennent de leur coeur, Qu&#39;ils ne se convertissent, et que je ne les gu&eacute;risse.</p>

<p><sup class="versenum">28&nbsp;</sup>Sachez donc que ce salut de Dieu a &eacute;t&eacute; envoy&eacute; aux pa&iuml;ens, et qu&#39;ils l&#39;&eacute;couteront.</p>

<p><sup class="versenum">29&nbsp;</sup>Lorsqu&#39;il eut dit cela, les Juifs s&#39;en all&egrave;rent, discutant vivement entre eux.</p>

<p><sup class="versenum">30&nbsp;</sup>Paul demeura deux ans entiers dans une maison qu&#39;il avait lou&eacute;e. Il recevait tous ceux qui venaient le voir,</p>

<p><sup class="versenum">31&nbsp;</sup>pr&ecirc;chant le royaume de Dieu et enseignant ce qui concerne le Seigneur J&eacute;sus Christ, en toute libert&eacute; et sans obstacle.</p>

<p>&nbsp;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/354.mp4" type="button" class="external-movie">
         Regardez Actes 28:11-31 </button>
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
	<li class="nobreak-final-final">Les croyants romains auraient re&ccedil;u la lettre de Paul il y a 3 ans plus t&ocirc;t. Paul a gard&eacute; le mod&egrave;le qui est de commencer par les Juifs, leur donnant la preuve &agrave; partir de l&#39;&Eacute;criture que J&eacute;sus est le Messie, puis de commencer &agrave; partager avec le peuple non juif. Le t&eacute;moignage du dirigeant juif a donn&eacute; un aper&ccedil;u de l&rsquo;expansion de l&rsquo;&Eacute;vangile, &laquo;nous savons que que cette secte rencontre partout de l&rsquo;opposition&raquo; (<span class="popup-link" @click = "popUp('pop3')"> Actes 28:22</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">22&nbsp;</sup>Mais nous voudrions apprendre de toi ce que tu penses, car nous savons que cette secte rencontre partout de l&#39;opposition.</p>
	<!-- end bible --></div>
	Paul pouvait t&eacute;moigner devant ses gardes romains et m&ecirc;me des membres de la maison de C&eacute;sar ont cru (<span class="popup-link" @click = "popUp('pop4')"> Philippiens 4:22</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">22&nbsp;</sup>Tous les saints vous saluent, et principalement ceux de la maison de C&eacute;sar.</p>
	<!-- end bible --></div>
	Pendant son s&eacute;jour &agrave; Rome, Paul a continu&eacute; &agrave; coacher et &agrave; conseiller les croyants de Philippes, Colosse et &Eacute;ph&egrave;se par la r&eacute;daction de lettres.</li>
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

			<td class="social" @click="share('lesson', 'Ministère en étant dans une maison d\'arrêt à Rome: ', '/content/M2/fra/multiply3/multiply354.html')">
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