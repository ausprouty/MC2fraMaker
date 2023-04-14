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
                        <div class="chapter_number ltr"><h1>25.</h1></div>
                        <div class="chapter_title ltr"><h1>Implantation d'église dans la capitale de Galatie  (Antioche de Pisidie)</h1></div>
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
	<li>Lisez ou observez Actes 13:13-43 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 13:13-43</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">13&nbsp;</sup>Paul et ses compagnons, s&#39;&eacute;tant embarqu&eacute;s &agrave; Paphos, se rendirent &agrave; Perge en Pamphylie. Jean se s&eacute;para d&#39;eux, et retourna &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">14&nbsp;</sup>De Perge ils poursuivirent leur route, et arriv&egrave;rent &agrave; Antioche de Pisidie. &Eacute;tant entr&eacute;s dans la synagogue le jour du sabbat, ils s&#39;assirent.</p>

<p><sup class="versenum">15&nbsp;</sup>Apr&egrave;s la lecture de la loi et des proph&egrave;tes, les chefs de la synagogue leur envoy&egrave;rent dire: Hommes fr&egrave;res, si vous avez quelque exhortation &agrave; adresser au peuple, parlez.</p>

<p><sup class="versenum">16&nbsp;</sup>Paul se leva, et, ayant fait signe de la main, il dit: Hommes Isra&eacute;lites, et vous qui craignez Dieu, &eacute;coutez!</p>

<p><sup class="versenum">17&nbsp;</sup>Le Dieu de ce peuple d&#39;Isra&euml;l a choisi nos p&egrave;res. Il mit ce peuple en honneur pendant son s&eacute;jour au pays d&#39;&Eacute;gypte, et il l&#39;en fit sortir par son bras puissant.</p>

<p><sup class="versenum">18&nbsp;</sup>Il les nourrit pr&egrave;s de quarante ans dans le d&eacute;sert;</p>

<p><sup class="versenum">19&nbsp;</sup>et, ayant d&eacute;truit sept nations au pays de Canaan, il leur en accorda le territoire comme propri&eacute;t&eacute;.</p>

<p><sup class="versenum">20&nbsp;</sup>Apr&egrave;s cela, durant quatre cent cinquante ans environ, il leur donna des juges, jusqu&#39;au proph&egrave;te Samuel.</p>

<p><sup class="versenum">21&nbsp;</sup>Ils demand&egrave;rent alors un roi. Et Dieu leur donna, pendant quarante ans, Sa&uuml;l, fils de Kis, de la tribu de Benjamin;</p>

<p><sup class="versenum">22&nbsp;</sup>puis, l&#39;ayant rejet&eacute;, il leur suscita pour roi David, auquel il a rendu ce t&eacute;moignage: J&#39;ai trouv&eacute; David, fils d&#39;Isa&iuml;, homme selon mon coeur, qui accomplira toutes mes volont&eacute;s.</p>

<p><sup class="versenum">23&nbsp;</sup>C&#39;est de la post&eacute;rit&eacute; de David que Dieu, selon sa promesse, a suscit&eacute; &agrave; Isra&euml;l un Sauveur, qui est J&eacute;sus.</p>

<p><sup class="versenum">24&nbsp;</sup>Avant sa venue, Jean avait pr&ecirc;ch&eacute; le bapt&ecirc;me de repentance &agrave; tout le peuple d&#39;Isra&euml;l.</p>

<p><sup class="versenum">25&nbsp;</sup>Et lorsque Jean achevait sa course, il disait: Je ne suis pas celui que vous pensez; mais voici, apr&egrave;s moi vient celui des pieds duquel je ne suis pas digne de d&eacute;lier les souliers.</p>

<p><sup class="versenum">26&nbsp;</sup>Hommes fr&egrave;res, fils de la race d&#39;Abraham, et vous qui craignez Dieu, c&#39;est &agrave; vous que cette parole de salut a &eacute;t&eacute; envoy&eacute;e.</p>

<p><sup class="versenum">27&nbsp;</sup>Car les habitants de J&eacute;rusalem et leurs chefs ont m&eacute;connu J&eacute;sus, et, en le condamnant, ils ont accompli les paroles des proph&egrave;tes qui se lisent chaque sabbat.</p>

<p><sup class="versenum">28&nbsp;</sup>Quoiqu&#39;ils ne trouvassent en lui rien qui f&ucirc;t digne de mort, ils ont demand&eacute; &agrave; Pilate de le faire mourir.</p>

<p><sup class="versenum">29&nbsp;</sup>Et, apr&egrave;s qu&#39;ils eurent accompli tout ce qui est &eacute;crit de lui, ils le descendirent de la croix et le d&eacute;pos&egrave;rent dans un s&eacute;pulcre.</p>

<p><sup class="versenum">30&nbsp;</sup>Mais Dieu l&#39;a ressuscit&eacute; des morts.</p>

<p><sup class="versenum">31&nbsp;</sup>Il est apparu pendant plusieurs jours &agrave; ceux qui &eacute;taient mont&eacute;s avec lui de la Galil&eacute;e &agrave; J&eacute;rusalem, et qui sont maintenant ses t&eacute;moins aupr&egrave;s du peuple.</p>

<p><sup class="versenum">32&nbsp;</sup>Et nous, nous vous annon&ccedil;ons cette bonne nouvelle que la promesse faite &agrave; nos p&egrave;res,</p>

<p><sup class="versenum">33&nbsp;</sup>Dieu l&#39;a accomplie pour nous leurs enfants, en ressuscitant J&eacute;sus, selon ce qui est &eacute;crit dans le Psaume deuxi&egrave;me: Tu es mon Fils, Je t&#39;ai engendr&eacute; aujourd&#39;hui.</p>

<p><sup class="versenum">34&nbsp;</sup>Qu&#39;il l&#39;ait ressuscit&eacute; des morts, de telle sorte qu&#39;il ne retournera pas &agrave; la corruption, c&#39;est ce qu&#39;il a d&eacute;clar&eacute;, en disant: Je vous donnerai Les gr&acirc;ces saintes promises &agrave; David, ces gr&acirc;ces qui sont assur&eacute;es.</p>

<p><sup class="versenum">35&nbsp;</sup>C&#39;est pourquoi il dit encore ailleurs: Tu ne permettras pas que ton Saint voie la corruption.</p>

<p><sup class="versenum">36&nbsp;</sup>Or, David, apr&egrave;s avoir en son temps servi au dessein de Dieu, est mort, a &eacute;t&eacute; r&eacute;uni &agrave; ses p&egrave;res, et a vu la corruption.</p>

<p><sup class="versenum">37&nbsp;</sup>Mais celui que Dieu a ressuscit&eacute; n&#39;a pas vu la corruption.</p>

<p><sup class="versenum">38&nbsp;</sup>Sachez donc, hommes fr&egrave;res, que c&#39;est par lui que le pardon des p&eacute;ch&eacute;s vous est annonc&eacute;,</p>

<p><sup class="versenum">39&nbsp;</sup>et que quiconque croit est justifi&eacute; par lui de toutes les choses dont vous ne pouviez &ecirc;tre justifi&eacute;s par la loi de Mo&iuml;se.</p>

<p><sup class="versenum">40&nbsp;</sup>Ainsi, prenez garde qu&#39;il ne vous arrive ce qui est dit dans les proph&egrave;tes:</p>

<p><sup class="versenum">41&nbsp;</sup>Voyez, contempteurs, Soyez &eacute;tonn&eacute;s et disparaissez; Car je vais faire en vos jours une oeuvre, Une oeuvre que vous ne croiriez pas si on vous la racontait.</p>

<p><sup class="versenum">42&nbsp;</sup>Lorsqu&#39;ils sortirent, on les pria de parler le sabbat suivant sur les m&ecirc;mes choses;</p>

<p><sup class="versenum">43&nbsp;</sup>et, &agrave; l&#39;issue de l&#39;assembl&eacute;e, beaucoup de Juifs et de pros&eacute;lytes pieux suivirent Paul et Barnabas, qui s&#39;entretinrent avec eux, et les exhort&egrave;rent &agrave; rester attach&eacute;s &agrave; la gr&acirc;ce de Dieu.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/325.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 13:13-43&nbsp; </button>
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
	<li class="nobreak-final-final">Paul et Barnabas quittent Chypre pour la province de Pamphylie, o&ugrave; Jean-Marc d&eacute;cide de les quitter. En traversant l&rsquo;&Icirc;le vers le nord, ils atteignent Antioche de Pisidie, la capitale de la province montagneuse de Galatie. L&#39;histoire fournit un d&eacute;tail important des raisons pour lesquelles ils sont all&eacute;s dans cette ville. Le gouverneur de Chypre avait une famille dans cette ville, ce qui a pouss&eacute; Paul et Barnabas &agrave; continuer &agrave; suivre les r&eacute;seaux relationnels que le Seigneur ouvrait devant eux. Cette ville &eacute;tait &eacute;galement &agrave; un carrefour majeur des r&eacute;gions environnantes. Paul et Barnabas ont parl&eacute; dans la synagogue, sachant qu&#39;ils trouveraient des Juifs craignant Dieu et des non-Juifs spirituellement int&eacute;ress&eacute;s (<span class="popup-link" @click = "popUp('pop3')"> Actes 13:26</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">26&nbsp;</sup>Hommes fr&egrave;res, fils de la race d&#39;Abraham, et vous qui craignez Dieu, c&#39;est &agrave; vous que cette parole de salut a &eacute;t&eacute; envoy&eacute;e.</p>
	<!-- end bible --></div>
	Paul a utilis&eacute; des histoires tir&eacute;es des &Eacute;critures qui ont montr&eacute; que J&eacute;sus &eacute;tait la solution de Dieu pour leur p&eacute;ch&eacute; (<span class="popup-link" @click = "popUp('pop4')"> Actes 13: 38-39</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">38&nbsp;</sup>Sachez donc, hommes fr&egrave;res, que c&#39;est par lui que le pardon des p&eacute;ch&eacute;s vous est annonc&eacute;,</p>

	<p><sup class="versenum">39&nbsp;</sup>et que quiconque croit est justifi&eacute; par lui de toutes les choses dont vous ne pouviez &ecirc;tre justifi&eacute;s par la loi de Mo&iuml;se.</p>
	<!-- end bible --></div>
	Beaucoup ont cru. Paul et Barnabas ont donc fait un premier suivi en les encourageant &agrave; grandir dans leur relation avec Christ.</li>
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

			<td class="social" @click="share('lesson', 'Implantation d\'église dans la capitale de Galatie  (Antioche de Pisidie): ', '/content/M2/fra/multiply3/multiply325.html')">
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