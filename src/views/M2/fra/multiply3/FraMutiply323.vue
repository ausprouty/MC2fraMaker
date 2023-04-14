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
                        <div class="chapter_number ltr"><h1>23.</h1></div>
                        <div class="chapter_title ltr"><h1>Le roi Hérode persécute les leaders et Dieu réagit</h1></div>
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
	<li>Lisez ou observez Actes 12:1-25 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 12</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Vers le m&ecirc;me temps, le roi H&eacute;rode se mit &agrave; maltraiter quelques membres de l&#39;&Eacute;glise,</p>

<p><sup class="versenum">2&nbsp;</sup>et il fit mourir par l&#39;&eacute;p&eacute;e Jacques, fr&egrave;re de Jean.</p>

<p><sup class="versenum">3&nbsp;</sup>Voyant que cela &eacute;tait agr&eacute;able aux Juifs, il fit encore arr&ecirc;ter Pierre. -C&#39;&eacute;tait pendant les jours des pains sans levain. -</p>

<p><sup class="versenum">4&nbsp;</sup>Apr&egrave;s l&#39;avoir saisi et jet&eacute; en prison, il le mit sous la garde de quatre escouades de quatre soldats chacune, avec l&#39;intention de le faire compara&icirc;tre devant le peuple apr&egrave;s la P&acirc;que.</p>

<p><sup class="versenum">5&nbsp;</sup>Pierre donc &eacute;tait gard&eacute; dans la prison; et l&#39;&Eacute;glise ne cessait d&#39;adresser pour lui des pri&egrave;res &agrave; Dieu.</p>

<p><sup class="versenum">6&nbsp;</sup>La nuit qui pr&eacute;c&eacute;da le jour o&ugrave; H&eacute;rode allait le faire compara&icirc;tre, Pierre, li&eacute; de deux cha&icirc;nes, dormait entre deux soldats; et des sentinelles devant la porte gardaient la prison.</p>

<p><sup class="versenum">7&nbsp;</sup>Et voici, un ange du Seigneur survint, et une lumi&egrave;re brilla dans la prison. L&#39;ange r&eacute;veilla Pierre, en le frappant au c&ocirc;t&eacute;, et en disant: L&egrave;ve-toi promptement! Les cha&icirc;nes tomb&egrave;rent de ses mains.</p>

<p><sup class="versenum">8&nbsp;</sup>Et l&#39;ange lui dit: Mets ta ceinture et tes sandales. Et il fit ainsi. L&#39;ange lui dit encore: Enveloppe-toi de ton manteau, et suis-moi.</p>

<p><sup class="versenum">9&nbsp;</sup>Pierre sortit, et le suivit, ne sachant pas que ce qui se faisait par l&#39;ange f&ucirc;t r&eacute;el, et s&#39;imaginant avoir une vision.</p>

<p><sup class="versenum">10&nbsp;</sup>Lorsqu&#39;ils eurent pass&eacute; la premi&egrave;re garde, puis la seconde, ils arriv&egrave;rent &agrave; la porte de fer qui m&egrave;ne &agrave; la ville, et qui s&#39;ouvrit d&#39;elle-m&ecirc;me devant eux; ils sortirent, et s&#39;avanc&egrave;rent dans une rue. Aussit&ocirc;t l&#39;ange quitta Pierre.</p>

<p><sup class="versenum">11&nbsp;</sup>Revenu &agrave; lui-m&ecirc;me, Pierre dit: Je vois maintenant d&#39;une mani&egrave;re certaine que le Seigneur a envoy&eacute; son ange, et qu&#39;il m&#39;a d&eacute;livr&eacute; de la main d&#39;H&eacute;rode et de tout ce que le peuple juif attendait.</p>

<p><sup class="versenum">12&nbsp;</sup>Apr&egrave;s avoir r&eacute;fl&eacute;chi, il se dirigea vers la maison de Marie, m&egrave;re de Jean, surnomm&eacute; Marc, o&ugrave; beaucoup de personnes &eacute;taient r&eacute;unies et priaient.</p>

<p><sup class="versenum">13&nbsp;</sup>Il frappa &agrave; la porte du vestibule, et une servante, nomm&eacute;e Rhode, s&#39;approcha pour &eacute;couter.</p>

<p><sup class="versenum">14&nbsp;</sup>Elle reconnut la voix de Pierre; et, dans sa joie, au lieu d&#39;ouvrir, elle courut annoncer que Pierre &eacute;tait devant la porte.</p>

<p><sup class="versenum">15&nbsp;</sup>Ils lui dirent: Tu es folle. Mais elle affirma que la chose &eacute;tait ainsi.</p>

<p><sup class="versenum">16&nbsp;</sup>Et ils dirent: C&#39;est son ange. Cependant Pierre continuait &agrave; frapper. Ils ouvrirent, et furent &eacute;tonn&eacute;s de le voir.</p>

<p><sup class="versenum">17&nbsp;</sup>Pierre, leur ayant de la main fait signe de se taire, leur raconta comment le Seigneur l&#39;avait tir&eacute; de la prison, et il dit: Annoncez-le &agrave; Jacques et aux fr&egrave;res. Puis il sortit, et s&#39;en alla dans un autre lieu.</p>

<p><sup class="versenum">18&nbsp;</sup>Quand il fit jour, les soldats furent dans une grande agitation, pour savoir ce que Pierre &eacute;tait devenu.</p>

<p><sup class="versenum">19&nbsp;</sup>H&eacute;rode, s&#39;&eacute;tant mis &agrave; sa recherche et ne l&#39;ayant pas trouv&eacute;, interrogea les gardes, et donna l&#39;ordre de les mener au supplice. Ensuite il descendit de la Jud&eacute;e &agrave; C&eacute;sar&eacute;e, pour y s&eacute;journer.</p>

<p><sup class="versenum">20&nbsp;</sup>H&eacute;rode avait des dispositions hostiles &agrave; l&#39;&eacute;gard des Tyriens et des Sidoniens. Mais ils vinrent le trouver d&#39;un commun accord; et, apr&egrave;s avoir gagn&eacute; Blaste, son chambellan, ils sollicit&egrave;rent la paix, parce que leur pays tirait sa subsistance de celui du roi.</p>

<p><sup class="versenum">21&nbsp;</sup>A un jour fix&eacute;, H&eacute;rode, rev&ecirc;tu de ses habits royaux, et assis sur son tr&ocirc;ne, les harangua publiquement.</p>

<p><sup class="versenum">22&nbsp;</sup>Le peuple s&#39;&eacute;cria: Voix d&#39;un dieu, et non d&#39;un homme!</p>

<p><sup class="versenum">23&nbsp;</sup>Au m&ecirc;me instant, un ange du Seigneur le frappa, parce qu&#39;il n&#39;avait pas donn&eacute; gloire &agrave; Dieu. Et il expira, rong&eacute; des vers.</p>

<p><sup class="versenum">24&nbsp;</sup>Cependant la parole de Dieu se r&eacute;pandait de plus en plus, et le nombre des disciples augmentait.</p>

<p><sup class="versenum">25&nbsp;</sup>Barnabas et Saul, apr&egrave;s s&#39;&ecirc;tre acquitt&eacute;s de leur message, s&#39;en retourn&egrave;rent de J&eacute;rusalem, emmenant avec eux Jean, surnomm&eacute; Marc.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/323.mp4" type="button" class="external-movie">
         Regardez Actes 12 </button>
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
	<li class="nobreak-final-final">J&eacute;sus a d&eacute;clar&eacute; au Ap&ocirc;tres que &laquo; S&rsquo;ils m&rsquo;ont pers&eacute;cut&eacute;, ils vous pers&eacute;cuteront aussi &raquo; (<span class="popup-link" @click = "popUp('pop3')"> Jean 15:20</span>).&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">20&nbsp;</sup>Souvenez-vous de la parole que je vous ai dite: Le serviteur n&#39;est pas plus grand que son ma&icirc;tre. S&#39;ils m&#39;ont pers&eacute;cut&eacute;, ils vous pers&eacute;cuteront aussi; s&#39;ils ont gard&eacute; ma parole, ils garderont aussi la v&ocirc;tre.</p>
	<!-- end bible --></div>
	En ce moment la pers&eacute;cution &eacute;clate contre les ap&ocirc;tres et d&rsquo;autres leaders d&lsquo;&eacute;glise. Le Seigneur a permet &agrave; ce que l&rsquo;ap&ocirc;tre Jacques &nbsp;tu&eacute; ; mais il permet &agrave; Pierre de s&rsquo;&eacute;chapper miraculeusement des mains d&rsquo;H&eacute;rode. Bien que les croyants fussent entrain de prier pour que Dieu sauve Pierre, certains d&rsquo;entre eux doutaient que cela puisse arriver (<span class="popup-link" @click = "popUp('pop4')"> Jean&nbsp;12 :13</span>).&nbsp;

	<div class="popup invisible" id="pop4">&nbsp;</div>
	&nbsp;La pers&eacute;cution n&rsquo;aboutit pas &agrave; un r&eacute;sultat: parfois les croyants &eacute;chappent ; d&rsquo;autre fois ils sont tu&eacute;s ; parfois Dieu fait un miracle et d&rsquo;autre fois il ne le fait pas. Le Seigneur enseigna &laquo; Aimez vos ennemis, et priez pour ceux qui vous maltraitent et qui vous pers&eacute;cutent &raquo; et &laquo; A moi la vengeance, &agrave; moi la r&eacute;tribution &raquo; (<span class="popup-link" @click = "popUp('pop5')"> Matthieu 5 :43-48</span>;&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">43&nbsp;</sup>Vous avez appris qu&#39;il a &eacute;t&eacute; dit: Tu aimeras ton prochain, et tu ha&iuml;ras ton ennemi.</p>

	<p><sup class="versenum">44&nbsp;</sup>Mais moi, je vous dis: Aimez vos ennemis, b&eacute;nissez ceux qui vous maudissent, faites du bien &agrave; ceux qui vous ha&iuml;ssent, et priez pour ceux qui vous maltraitent et qui vous pers&eacute;cutent,</p>

	<p><sup class="versenum">45&nbsp;</sup>afin que vous soyez fils de votre P&egrave;re qui est dans les cieux; car il fait lever son soleil sur les m&eacute;chants et sur les bons, et il fait pleuvoir sur les justes et sur les injustes.</p>

	<p><sup class="versenum">46&nbsp;</sup>Si vous aimez ceux qui vous aiment, quelle r&eacute;compense m&eacute;ritez-vous? Les publicains aussi n&#39;agissent-ils pas de m&ecirc;me?</p>

	<p><sup class="versenum">47&nbsp;</sup>Et si vous saluez seulement vos fr&egrave;res, que faites-vous d&#39;extraordinaire? Les pa&iuml;ens aussi n&#39;agissent-ils pas de m&ecirc;me?</p>

	<p><sup class="versenum">48&nbsp;</sup>Soyez donc parfaits, comme votre P&egrave;re c&eacute;leste est parfait.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop6')"> Romains 12 :17-21</span>).&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">17&nbsp;</sup>Ne rendez &agrave; personne le mal pour le mal. Recherchez ce qui est bien devant tous les hommes.</p>

	<p><sup class="versenum">18&nbsp;</sup>S&#39;il est possible, autant que cela d&eacute;pend de vous, soyez en paix avec tous les hommes.</p>

	<p><sup class="versenum">19&nbsp;</sup>Ne vous vengez point vous-m&ecirc;mes, bien-aim&eacute;s, mais laissez agir la col&egrave;re; car il est &eacute;crit: A moi la vengeance, &agrave; moi la r&eacute;tribution, dit le Seigneur.</p>

	<p><sup class="versenum">20&nbsp;</sup>Mais si ton ennemi a faim, donne-lui &agrave; manger; s&#39;il a soif, donne-lui &agrave; boire; car en agissant ainsi, ce sont des charbons ardents que tu amasseras sur sa t&ecirc;te.</p>

	<p><sup class="versenum">21&nbsp;</sup>Ne te laisse pas vaincre par le mal, mais surmonte le mal par le bien.</p>
	<!-- end bible --></div>
	&nbsp;Pendant ce temps Dieu r&eacute;agit &agrave; l&rsquo;arrogance et &agrave; l&rsquo;attaque d&rsquo;H&eacute;rode en le supprimant tout en continuant &agrave; r&eacute;pandre sa propre Parole. &nbsp;Cette histoire comprend la troisi&egrave;me d&eacute;claration sommaire trouv&eacute;e dans le livre des Actes : la parole de Dieu se r&eacute;pandait et se multipliait. (<span class="popup-link" @click = "popUp('pop7')"> Actes 12: 24</span>).&nbsp;

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">24&nbsp;</sup>Cependant la parole de Dieu se r&eacute;pandait de plus en plus, et le nombre des disciples augmentait.</p>
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

			<td class="social" @click="share('lesson', 'Le roi Hérode persécute les leaders et Dieu réagit: ', '/content/M2/fra/multiply3/mutiply323.html')">
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