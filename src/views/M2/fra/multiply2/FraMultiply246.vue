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
                        <div class="chapter_number ltr"><h1>46.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership Passionné</h1></div>
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
	<li>Lisez ou observez Luc 19:28-48 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 19:28-48</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">28&nbsp;</sup>Apr&egrave;s avoir ainsi parl&eacute;, J&eacute;sus marcha devant la foule, pour monter &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">29&nbsp;</sup>Lorsqu&#39;il approcha de Bethphag&eacute; et de B&eacute;thanie, vers la montagne appel&eacute;e montagne des Oliviers, J&eacute;sus envoya deux de ses disciples,</p>

<p><sup class="versenum">30&nbsp;</sup>en disant: Allez au village qui est en face; quand vous y serez entr&eacute;s, vous trouverez un &acirc;non attach&eacute;, sur lequel aucun homme ne s&#39;est jamais assis; d&eacute;tachez-le, et amenez-le.</p>

<p><sup class="versenum">31&nbsp;</sup>Si quelqu&#39;un vous demande: Pourquoi le d&eacute;tachez-vous? vous lui r&eacute;pondrez: Le Seigneur en a besoin.</p>

<p><sup class="versenum">32&nbsp;</sup>Ceux qui &eacute;taient envoy&eacute;s all&egrave;rent, et trouv&egrave;rent les choses comme J&eacute;sus leur avait dit.</p>

<p><sup class="versenum">33&nbsp;</sup>Comme ils d&eacute;tachaient l&#39;&acirc;non, ses ma&icirc;tres leur dirent: Pourquoi d&eacute;tachez-vous l&#39;&acirc;non?</p>

<p><sup class="versenum">34&nbsp;</sup>Ils r&eacute;pondirent: Le Seigneur en a besoin.</p>

<p><sup class="versenum">35&nbsp;</sup>Et ils amen&egrave;rent &agrave; J&eacute;sus l&#39;&acirc;non, sur lequel ils jet&egrave;rent leurs v&ecirc;tements, et firent monter J&eacute;sus.</p>

<p><sup class="versenum">36&nbsp;</sup>Quand il fut en marche, les gens &eacute;tendirent leurs v&ecirc;tements sur le chemin.</p>

<p><sup class="versenum">37&nbsp;</sup>Et lorsque d&eacute;j&agrave; il approchait de J&eacute;rusalem, vers la descente de la montagne des Oliviers, toute la multitude des disciples, saisie de joie, se mit &agrave; louer Dieu &agrave; haute voix pour tous les miracles qu&#39;ils avaient vus.</p>

<p><sup class="versenum">38&nbsp;</sup>Ils disaient: B&eacute;ni soit le roi qui vient au nom du Seigneur! Paix dans le ciel, et gloire dans les lieux tr&egrave;s hauts!</p>

<p><sup class="versenum">39&nbsp;</sup>Quelques pharisiens, du milieu de la foule, dirent &agrave; J&eacute;sus: Ma&icirc;tre, reprends tes disciples.</p>

<p><sup class="versenum">40&nbsp;</sup>Et il r&eacute;pondit: Je vous le dis, s&#39;ils se taisent, les pierres crieront!</p>

<p><sup class="versenum">41&nbsp;</sup>Comme il approchait de la ville, J&eacute;sus, en la voyant, pleura sur elle, et dit:</p>

<p><sup class="versenum">42&nbsp;</sup>Si toi aussi, au moins en ce jour qui t&#39;est donn&eacute;, tu connaissais les choses qui appartiennent &agrave; ta paix! Mais maintenant elles sont cach&eacute;es &agrave; tes yeux.</p>

<p><sup class="versenum">43&nbsp;</sup>Il viendra sur toi des jours o&ugrave; tes ennemis t&#39;environneront de tranch&eacute;es, t&#39;enfermeront, et te serreront de toutes parts;</p>

<p><sup class="versenum">44&nbsp;</sup>ils te d&eacute;truiront, toi et tes enfants au milieu de toi, et ils ne laisseront pas en toi pierre sur pierre, parce que tu n&#39;as pas connu le temps o&ugrave; tu as &eacute;t&eacute; visit&eacute;e.</p>

<p><sup class="versenum">45&nbsp;</sup>Il entra dans le temple, et il se mit &agrave; chasser ceux qui vendaient,</p>

<p><sup class="versenum">46&nbsp;</sup>leur disant: Il est &eacute;crit: Ma maison sera une maison de pri&egrave;re. Mais vous, vous en avez fait une caverne de voleurs.</p>

<p><sup class="versenum">47&nbsp;</sup>Il enseignait tous les jours dans le temple. Et les principaux sacrificateurs, les scribes, et les principaux du peuple cherchaient &agrave; le faire p&eacute;rir;</p>

<p><sup class="versenum">48&nbsp;</sup>mais ils ne savaient comment s&#39;y prendre, car tout le peuple l&#39;&eacute;coutait avec admiration.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/246.mp4" type="button" class="external-movie">
         Regardez Luc 19:28-48 </button>
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

<p>Une proph&eacute;tie donn&eacute;e 500 ans plus t&ocirc;t se r&eacute;alise devant ces jeunes leaders. Un roi mont&eacute; sur un &acirc;ne! (Zacharie 9: 9). Les gens louaient Dieu alors que J&eacute;sus descendait de la Montagne des Oliviers et prenait la route vers la ville de J&eacute;rusalem. Les pharisiens ont compris les implications messianiques de la situation et ont dit &agrave; J&eacute;sus de dire &agrave; ses disciples d&#39;arr&ecirc;ter. Mais J&eacute;sus connaissait l&#39;importance de ce t&eacute;moignage dans le plan du P&egrave;re. Alors que J&eacute;sus s&#39;approche de la ville, il commence &agrave; pleurer. Il &eacute;tait attrist&eacute; parce qu&#39;il savait que la plupart des gens ne r&eacute;alisaient pas qui Il &eacute;tait et la signification de l&#39;&eacute;v&eacute;nement. Il savait aussi qu&#39;un jour, le jugement viendrait sur la ville &agrave; cause de leur incr&eacute;dulit&eacute; et la ville de J&eacute;rusalem serait d&eacute;truite par l&#39;arm&eacute;e romaine. Une fois de plus, nous voyons la passion de J&eacute;sus affich&eacute;e quand Il chasse les changeurs d&#39;argent qui sont revenus &agrave; leurs vieilles pratiques en profitant des gens qui viennent adorer Dieu. J&eacute;sus n&#39;a pas seulement montr&eacute; de la passion pour la r&eacute;putation du P&egrave;re, mais aussi de la compassion pour les pauvres et les &eacute;trangers.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Matthieu 21 :1-17</span>;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Lorsqu&#39;ils approch&egrave;rent de J&eacute;rusalem, et qu&#39;ils furent arriv&eacute;s &agrave; Bethphag&eacute;, vers la montagne des Oliviers, J&eacute;sus envoya deux disciples,</p>

	<p><sup class="versenum">2&nbsp;</sup>en leur disant: Allez au village qui est devant vous; vous trouverez aussit&ocirc;t une &acirc;nesse attach&eacute;e, et un &acirc;non avec elle; d&eacute;tachez-les, et amenez-les-moi.</p>

	<p><sup class="versenum">3&nbsp;</sup>Si, quelqu&#39;un vous dit quelque chose, vous r&eacute;pondrez: Le Seigneur en a besoin. Et &agrave; l&#39;instant il les laissera aller.</p>

	<p><sup class="versenum">4&nbsp;</sup>Or, ceci arriva afin que s&#39;accompl&icirc;t ce qui avait &eacute;t&eacute; annonc&eacute; par le proph&egrave;te:</p>

	<p><sup class="versenum">5&nbsp;</sup>Dites &agrave; la fille de Sion: Voici, ton roi vient &agrave; toi, Plein de douceur, et mont&eacute; sur un &acirc;ne, Sur un &acirc;non, le petit d&#39;une &acirc;nesse.</p>

	<p><sup class="versenum">6&nbsp;</sup>Les disciples all&egrave;rent, et firent ce que J&eacute;sus leur avait ordonn&eacute;.</p>

	<p><sup class="versenum">7&nbsp;</sup>Ils amen&egrave;rent l&#39;&acirc;nesse et l&#39;&acirc;non, mirent sur eux leurs v&ecirc;tements, et le firent asseoir dessus.</p>

	<p><sup class="versenum">8&nbsp;</sup>La plupart des gens de la foule &eacute;tendirent leurs v&ecirc;tements sur le chemin; d&#39;autres coup&egrave;rent des branches d&#39;arbres, et en jonch&egrave;rent la route.</p>

	<p><sup class="versenum">9&nbsp;</sup>Ceux qui pr&eacute;c&eacute;daient et ceux qui suivaient J&eacute;sus criaient: Hosanna au Fils de David! B&eacute;ni soit celui qui vient au nom du Seigneur! Hosanna dans les lieux tr&egrave;s hauts!</p>

	<p><sup class="versenum">10&nbsp;</sup>Lorsqu&#39;il entra dans J&eacute;rusalem, toute la ville fut &eacute;mue, et l&#39;on disait: Qui est celui-ci?</p>

	<p><sup class="versenum">11&nbsp;</sup>La foule r&eacute;pondait: C&#39;est J&eacute;sus, le proph&egrave;te, de Nazareth en Galil&eacute;e.</p>

	<p><sup class="versenum">12&nbsp;</sup>J&eacute;sus entra dans le temple de Dieu. Il chassa tous ceux qui vendaient et qui achetaient dans le temple; il renversa les tables des changeurs, et les si&egrave;ges des vendeurs de pigeons.</p>

	<p><sup class="versenum">13&nbsp;</sup>Et il leur dit: Il est &eacute;crit: Ma maison sera appel&eacute;e une maison de pri&egrave;re. Mais vous, vous en faites une caverne de voleurs.</p>

	<p><sup class="versenum">14&nbsp;</sup>Des aveugles et des boiteux s&#39;approch&egrave;rent de lui dans le temple. Et il les gu&eacute;rit.</p>

	<p><sup class="versenum">15&nbsp;</sup>Mais les principaux sacrificateurs et les scribes furent indign&eacute;s, &agrave; la vue des choses merveilleuses qu&#39;il avait faites, et des enfants qui criaient dans le temple: Hosanna au Fils de David!</p>

	<p><sup class="versenum">16&nbsp;</sup>Ils lui dirent: Entends-tu ce qu&#39;ils disent? Oui, leur r&eacute;pondit J&eacute;sus. N&#39;avez-vous jamais lu ces paroles: Tu as tir&eacute; des louanges de la bouche des enfants et de ceux qui sont &agrave; la mamelle?</p>

	<p><sup class="versenum">17&nbsp;</sup>Et, les ayant laiss&eacute;s, il sortit de la ville pour aller &agrave; B&eacute;thanie, o&ugrave; il passa la nuit.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Marc 11 :1-26</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Lorsqu&#39;ils approch&egrave;rent de J&eacute;rusalem, et qu&#39;ils furent pr&egrave;s de Bethphag&eacute; et de B&eacute;thanie, vers la montagne des oliviers, J&eacute;sus envoya deux de ses disciples,</p>

	<p><sup class="versenum">2&nbsp;</sup>en leur disant: Allez au village qui est devant vous; d&egrave;s que vous y serez entr&eacute;s, vous trouverez un &acirc;non attach&eacute;, sur lequel aucun homme ne s&#39;est encore assis; d&eacute;tachez-le, et amenez-le.</p>

	<p><sup class="versenum">3&nbsp;</sup>Si quelqu&#39;un vous dit: Pourquoi faites-vous cela? r&eacute;pondez: Le Seigneur en a besoin. Et &agrave; l&#39;instant il le laissera venir ici.</p>

	<p><sup class="versenum">4&nbsp;</sup>les disciples, &eacute;tant all&eacute;s, trouv&egrave;rent l&#39;&acirc;non attach&eacute; dehors pr&egrave;s d&#39;une porte, au contour du chemin, et ils le d&eacute;tach&egrave;rent.</p>

	<p><sup class="versenum">5&nbsp;</sup>Quelques-uns de ceux qui &eacute;taient l&agrave; leur dirent: Que faites-vous? pourquoi d&eacute;tachez-vous cet &acirc;non?</p>

	<p><sup class="versenum">6&nbsp;</sup>Ils r&eacute;pondirent comme J&eacute;sus l&#39;avait dit. Et on les laissa aller.</p>

	<p><sup class="versenum">7&nbsp;</sup>Ils amen&egrave;rent &agrave; J&eacute;sus l&#39;&acirc;non, sur lequel ils jet&egrave;rent leurs v&ecirc;tements, et J&eacute;sus s&#39;assit dessus.</p>

	<p><sup class="versenum">8&nbsp;</sup>Beaucoup de gens &eacute;tendirent leurs v&ecirc;tements sur le chemin, et d&#39;autres des branches qu&#39;ils coup&egrave;rent dans les champs.</p>

	<p><sup class="versenum">9&nbsp;</sup>Ceux qui pr&eacute;c&eacute;daient et ceux qui suivaient J&eacute;sus criaient: Hosanna! B&eacute;ni soit celui qui vient au nom du Seigneur!</p>

	<p><sup class="versenum">10&nbsp;</sup>B&eacute;ni soit le r&egrave;gne qui vient, le r&egrave;gne de David, notre p&egrave;re! Hosanna dans les lieux tr&egrave;s hauts!</p>

	<p><sup class="versenum">11&nbsp;</sup>J&eacute;sus entra &agrave; J&eacute;rusalem, dans le temple. Quand il eut tout consid&eacute;r&eacute;, comme il &eacute;tait d&eacute;j&agrave; tard, il s&#39;en alla &agrave; B&eacute;thanie avec les douze.</p>

	<p><sup class="versenum">12&nbsp;</sup>Le lendemain, apr&egrave;s qu&#39;ils furent sortis de B&eacute;thanie, J&eacute;sus eut faim.</p>

	<p><sup class="versenum">13&nbsp;</sup>Apercevant de loin un figuier qui avait des feuilles, il alla voir s&#39;il y trouverait quelque chose; et, s&#39;en &eacute;tant approch&eacute;, il ne trouva que des feuilles, car ce n&#39;&eacute;tait pas la saison des figues.</p>

	<p><sup class="versenum">14&nbsp;</sup>Prenant alors la parole, il lui dit: Que jamais personne ne mange de ton fruit! Et ses disciples l&#39;entendirent.</p>

	<p><sup class="versenum">15&nbsp;</sup>Ils arriv&egrave;rent &agrave; J&eacute;rusalem, et J&eacute;sus entra dans le temple. Il se mit &agrave; chasser ceux qui vendaient et qui achetaient dans le temple; il renversa les tables des changeurs, et les si&egrave;ges des vendeurs de pigeons;</p>

	<p><sup class="versenum">16&nbsp;</sup>et il ne laissait personne transporter aucun objet &agrave; travers le temple.</p>

	<p><sup class="versenum">17&nbsp;</sup>Et il enseignait et disait: N&#39;est-il pas &eacute;crit: Ma maison sera appel&eacute;e une maison de pri&egrave;re pour toutes les nations? Mais vous, vous en avez fait une caverne de voleurs.</p>

	<p><sup class="versenum">18&nbsp;</sup>Les principaux sacrificateurs et les scribes, l&#39;ayant entendu, cherch&egrave;rent les moyens de le faire p&eacute;rir; car ils le craignaient, parce que toute la foule &eacute;tait frapp&eacute;e de sa doctrine.</p>

	<p><sup class="versenum">19&nbsp;</sup>Quand le soir fut venu, J&eacute;sus sortit de la ville.</p>

	<p><sup class="versenum">20&nbsp;</sup>Le matin, en passant, les disciples virent le figuier s&eacute;ch&eacute; jusqu&#39;aux racines.</p>

	<p><sup class="versenum">21&nbsp;</sup>Pierre, se rappelant ce qui s&#39;&eacute;tait pass&eacute;, dit &agrave; J&eacute;sus: Rabbi, regarde, le figuier que tu as maudit a s&eacute;ch&eacute;.</p>

	<p><sup class="versenum">22&nbsp;</sup>J&eacute;sus prit la parole, et leur dit: Ayez foi en Dieu.</p>

	<p><sup class="versenum">23&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;, si quelqu&#39;un dit &agrave; cette montagne: Ote-toi de l&agrave; et jette-toi dans la mer, et s&#39;il ne doute point en son coeur, mais croit que ce qu&#39;il dit arrive, il le verra s&#39;accomplir.</p>

	<p><sup class="versenum">24&nbsp;</sup>C&#39;est pourquoi je vous dis: Tout ce que vous demanderez en priant, croyez que vous l&#39;avez re&ccedil;u, et vous le verrez s&#39;accomplir.</p>

	<p><sup class="versenum">25&nbsp;</sup>Et, lorsque vous &ecirc;tes debout faisant votre pri&egrave;re, si vous avez quelque chose contre quelqu&#39;un, pardonnez, afin que votre P&egrave;re qui est dans les cieux vous pardonne aussi vos offenses.</p>

	<p><sup class="versenum">26&nbsp;</sup>Mais si vous ne pardonnez pas, votre P&egrave;re qui est dans les cieux ne vous pardonnera pas non plus vos offenses.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop3')"> Jean 12:12-19</span>.

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>Le lendemain, une foule nombreuse de gens venus &agrave; la f&ecirc;te ayant entendu dire que J&eacute;sus se rendait &agrave; J&eacute;rusalem,</p>

	<p><sup class="versenum">13&nbsp;</sup>prirent des branches de palmiers, et all&egrave;rent au-devant de lui, en criant: Hosanna! B&eacute;ni soit celui qui vient au nom du Seigneur, le roi d&#39;Isra&euml;l!</p>

	<p><sup class="versenum">14&nbsp;</sup>J&eacute;sus trouva un &acirc;non, et s&#39;assit dessus, selon ce qui est &eacute;crit:</p>

	<p><sup class="versenum">15&nbsp;</sup>Ne crains point, fille de Sion; Voici, ton roi vient, Assis sur le petit d&#39;une &acirc;nesse.</p>

	<p><sup class="versenum">16&nbsp;</sup>Ses disciples ne comprirent pas d&#39;abord ces choses; mais, lorsque J&eacute;sus eut &eacute;t&eacute; glorifi&eacute;, ils se souvinrent qu&#39;elles &eacute;taient &eacute;crites de lui, et qu&#39;il les avaient &eacute;t&eacute; accomplies &agrave; son &eacute;gard.</p>

	<p><sup class="versenum">17&nbsp;</sup>Tous ceux qui &eacute;taient avec J&eacute;sus, quand il appela Lazare du s&eacute;pulcre et le ressuscita des morts, lui rendaient t&eacute;moignage;</p>

	<p><sup class="versenum">18&nbsp;</sup>et la foule vint au-devant de lui, parce qu&#39;elle avait appris qu&#39;il avait fait ce miracle.</p>

	<p><sup class="versenum">19&nbsp;</sup>Les pharisiens se dirent donc les uns aux autres: Vous voyez que vous ne gagnez rien; voici, le monde est all&eacute; apr&egrave;s lui.</p>
	<!-- end bible --></div>
	</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Leadership Passionné: ', '/content/M2/fra/multiply2/multiply246.html')">
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