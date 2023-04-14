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
                        <div class="chapter_number ltr"><h1>12.</h1></div>
                        <div class="chapter_title ltr"><h1>La défense d'Étienne devant le Sanhédrin</h1></div>
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
	<li>Lisez ou observez Actes 7:1-53 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 7:1-53</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Le souverain sacrificateur dit: Les choses sont-elles ainsi?</p>

<p><sup class="versenum">2&nbsp;</sup>&Eacute;tienne r&eacute;pondit: Hommes fr&egrave;res et p&egrave;res, &eacute;coutez! Le Dieu de gloire apparut &agrave; notre p&egrave;re Abraham, lorsqu&#39;il &eacute;tait en M&eacute;sopotamie, avant qu&#39;il s&#39;&eacute;tabl&icirc;t &agrave; Charran; et il lui dit:</p>

<p><sup class="versenum">3&nbsp;</sup>Quitte ton pays et ta famille, et va dans le pays que je te montrerai.</p>

<p><sup class="versenum">4&nbsp;</sup>Il sortit alors du pays des Chald&eacute;ens, et s&#39;&eacute;tablit &agrave; Charran. De l&agrave;, apr&egrave;s la mort de son p&egrave;re, Dieu le fit passer dans ce pays que vous habitez maintenant;</p>

<p><sup class="versenum">5&nbsp;</sup>il ne lui donna aucune propri&eacute;t&eacute; en ce pays, pas m&ecirc;me de quoi poser le pied, mais il promit de lui en donner la possession, et &agrave; sa post&eacute;rit&eacute; apr&egrave;s lui, quoiqu&#39;il n&#39;e&ucirc;t point d&#39;enfant.</p>

<p><sup class="versenum">6&nbsp;</sup>Dieu parla ainsi: Sa post&eacute;rit&eacute; s&eacute;journera dans un pays &eacute;tranger; on la r&eacute;duira en servitude et on la maltraitera pendant quatre cents ans.</p>

<p><sup class="versenum">7&nbsp;</sup>Mais la nation &agrave; laquelle ils auront &eacute;t&eacute; asservis, c&#39;est moi qui la jugerai, dit Dieu. Apr&egrave;s cela, ils sortiront, et ils me serviront dans ce lieu-ci.</p>

<p><sup class="versenum">8&nbsp;</sup>Puis Dieu donna &agrave; Abraham l&#39;alliance de la circoncision; et ainsi, Abraham, ayant engendr&eacute; Isaac, le circoncit le huiti&egrave;me jour; Isaac engendra et circoncit Jacob, et Jacob les douze patriarches.</p>

<p><sup class="versenum">9&nbsp;</sup>Les patriarches, jaloux de Joseph, le vendirent pour &ecirc;tre emmen&eacute; en &Eacute;gypte.</p>

<p><sup class="versenum">10&nbsp;</sup>Mais Dieu fut avec lui, et le d&eacute;livra de toutes ses tribulations; il lui donna de la sagesse et lui fit trouver gr&acirc;ce devant Pharaon, roi d&#39;&Eacute;gypte, qui l&#39;&eacute;tablit gouverneur d&#39;&Eacute;gypte et de toute sa maison.</p>

<p><sup class="versenum">11&nbsp;</sup>Il survint une famine dans tout le pays d&#39;&Eacute;gypte, et dans celui de Canaan. La d&eacute;tresse &eacute;tait grande, et nos p&egrave;res ne trouvaient pas de quoi se nourrir.</p>

<p><sup class="versenum">12&nbsp;</sup>Jacob apprit qu&#39;il y avait du bl&eacute; en &Eacute;gypte, et il y envoya nos p&egrave;res une premi&egrave;re fois.</p>

<p><sup class="versenum">13&nbsp;</sup>Et la seconde fois, Joseph fut reconnu par ses fr&egrave;res, et Pharaon sut de quelle famille il &eacute;tait.</p>

<p><sup class="versenum">14&nbsp;</sup>Puis Joseph envoya chercher son p&egrave;re Jacob, et toute sa famille, compos&eacute;e de soixante-quinze personnes.</p>

<p><sup class="versenum">15&nbsp;</sup>Jacob descendit en &Eacute;gypte, o&ugrave; il mourut, ainsi que nos p&egrave;res;</p>

<p><sup class="versenum">16&nbsp;</sup>et ils furent transport&eacute;s &agrave; Sichem, et d&eacute;pos&eacute;s dans le s&eacute;pulcre qu&#39;Abraham avait achet&eacute;, &agrave; prix d&#39;argent, des fils d&#39;H&eacute;mor, p&egrave;re de Sichem.</p>

<p><sup class="versenum">17&nbsp;</sup>Le temps approchait o&ugrave; devait s&#39;accomplir la promesse que Dieu avait faite &agrave; Abraham, et le peuple s&#39;accrut et se multiplia en &Eacute;gypte,</p>

<p><sup class="versenum">18&nbsp;</sup>jusqu&#39;&agrave; ce que parut un autre roi, qui n&#39;avait pas connu Joseph.</p>

<p><sup class="versenum">19&nbsp;</sup>Ce roi, usant d&#39;artifice contre notre race, maltraita nos p&egrave;res, au point de leur faire exposer leurs enfants, pour qu&#39;ils ne v&eacute;cussent pas.</p>

<p><sup class="versenum">20&nbsp;</sup>A cette &eacute;poque, naquit Mo&iuml;se, qui &eacute;tait beau aux yeux de Dieu. Il fut nourri trois mois dans la maison de son p&egrave;re;</p>

<p><sup class="versenum">21&nbsp;</sup>et, quand il eut &eacute;t&eacute; expos&eacute;, la fille de Pharaon le recueillit, et l&#39;&eacute;leva comme son fils.</p>

<p><sup class="versenum">22&nbsp;</sup>Mo&iuml;se fut instruit dans toute la sagesse des &Eacute;gyptiens, et il &eacute;tait puissant en paroles et en oeuvres.</p>

<p><sup class="versenum">23&nbsp;</sup>Il avait quarante ans, lorsqu&#39;il lui vint dans le coeur de visiter ses fr&egrave;res, les fils d&#39;Isra&euml;l.</p>

<p><sup class="versenum">24&nbsp;</sup>Il en vit un qu&#39;on outrageait, et, prenant sa d&eacute;fense, il vengea celui qui &eacute;tait maltrait&eacute;, et frappa l&#39;&Eacute;gyptien.</p>

<p><sup class="versenum">25&nbsp;</sup>Il pensait que ses fr&egrave;res comprendraient que Dieu leur accordait la d&eacute;livrance par sa main; mais ils ne comprirent pas.</p>

<p><sup class="versenum">26&nbsp;</sup>Le jour suivant, il parut au milieu d&#39;eux comme ils se battaient, et il les exhorta &agrave; la paix: Hommes, dit-il, vous &ecirc;tes fr&egrave;res; pourquoi vous maltraitez-vous l&#39;un l&#39;autre?</p>

<p><sup class="versenum">27&nbsp;</sup>Mais celui qui maltraitait son prochain le repoussa, en disant: Qui t&#39;a &eacute;tabli chef et juge sur nous?</p>

<p><sup class="versenum">28&nbsp;</sup>Veux-tu me tuer, comme tu as tu&eacute; hier l&#39;&Eacute;gyptien?</p>

<p><sup class="versenum">29&nbsp;</sup>A cette parole, Mo&iuml;se prit la fuite, et il alla s&eacute;journer dans le pays de Madian, o&ugrave; il engendra deux fils.</p>

<p><sup class="versenum">30&nbsp;</sup>Quarante ans plus tard, un ange lui apparut, au d&eacute;sert de la montagne de Sina&iuml;, dans la flamme d&#39;un buisson en feu.</p>

<p><sup class="versenum">31&nbsp;</sup>Mo&iuml;se, voyant cela, fut &eacute;tonn&eacute; de cette apparition; et, comme il s&#39;approchait pour examiner, la voix du Seigneur se fit entendre:</p>

<p><sup class="versenum">32&nbsp;</sup>Je suis le Dieu de tes p&egrave;res, le Dieu d&#39;Abraham, d&#39;Isaac et de Jacob. Et Mo&iuml;se, tout tremblant, n&#39;osait regarder.</p>

<p><sup class="versenum">33&nbsp;</sup>Le Seigneur lui dit: Ote tes souliers de tes pieds, car le lieu sur lequel tu te tiens est une terre sainte.</p>

<p><sup class="versenum">34&nbsp;</sup>J&#39;ai vu la souffrance de mon peuple qui est en &Eacute;gypte, j&#39;ai entendu ses g&eacute;missements, et je suis descendu pour le d&eacute;livrer. Maintenant, va, je t&#39;enverrai en &Eacute;gypte.</p>

<p><sup class="versenum">35&nbsp;</sup>Ce Mo&iuml;se, qu&#39;ils avaient reni&eacute;, en disant: Qui t&#39;a &eacute;tabli chef et juge? c&#39;est lui que Dieu envoya comme chef et comme lib&eacute;rateur avec l&#39;aide de l&#39;ange qui lui &eacute;tait apparu dans le buisson.</p>

<p><sup class="versenum">36&nbsp;</sup>C&#39;est lui qui les fit sortir d&#39;&Eacute;gypte, en op&eacute;rant des prodiges et des miracles au pays d&#39;&Eacute;gypte, au sein de la mer Rouge, et au d&eacute;sert, pendant quarante ans.</p>

<p><sup class="versenum">37&nbsp;</sup>C&#39;est ce Mo&iuml;se qui dit aux fils d&#39;Isra&euml;l: Dieu vous suscitera d&#39;entre vos fr&egrave;res un proph&egrave;te comme moi.</p>

<p><sup class="versenum">38&nbsp;</sup>C&#39;est lui qui, lors de l&#39;assembl&eacute;e au d&eacute;sert, &eacute;tant avec l&#39;ange qui lui parlait sur la montagne de Sina&iuml; et avec nos p&egrave;res, re&ccedil;ut des oracles vivants, pour nous les donner.</p>

<p><sup class="versenum">39&nbsp;</sup>Nos p&egrave;res ne voulurent pas lui ob&eacute;ir, ils le repouss&egrave;rent, et ils tourn&egrave;rent leur coeur vers l&#39;&Eacute;gypte,</p>

<p><sup class="versenum">40&nbsp;</sup>en disant &agrave; Aaron: Fais-nous des dieux qui marchent devant nous; car ce Mo&iuml;se qui nous a fait sortir du pays d&#39;&Eacute;gypte, nous ne savons ce qu&#39;il est devenu.</p>

<p><sup class="versenum">41&nbsp;</sup>Et, en ces jours-l&agrave;, ils firent un veau, ils offrirent un sacrifice &agrave; l&#39;idole, et se r&eacute;jouirent de l&#39;oeuvre de leurs mains.</p>

<p><sup class="versenum">42&nbsp;</sup>Alors Dieu se d&eacute;tourna, et les livra au culte de l&#39;arm&eacute;e du ciel, selon qu&#39;il est &eacute;crit dans le livre des proph&egrave;tes: M&#39;avez-vous offert des victimes et des sacrifices Pendant quarante ans au d&eacute;sert, maison d&#39;Isra&euml;l?...</p>

<p><sup class="versenum">43&nbsp;</sup>Vous avez port&eacute; la tente de Moloch Et l&#39;&eacute;toile du dieu Remphan, Ces images que vous avez faites pour les adorer! Aussi vous transporterai-je au del&agrave; de Babylone.</p>

<p><sup class="versenum">44&nbsp;</sup>Nos p&egrave;res avaient au d&eacute;sert le tabernacle du t&eacute;moignage, comme l&#39;avait ordonn&eacute; celui qui dit &agrave; Mo&iuml;se de le faire d&#39;apr&egrave;s le mod&egrave;le qu&#39;il avait vu.</p>

<p><sup class="versenum">45&nbsp;</sup>Et nos p&egrave;res, l&#39;ayant re&ccedil;u, l&#39;introduisirent, sous la conduite de Josu&eacute;, dans le pays qui &eacute;tait poss&eacute;d&eacute; par les nations que Dieu chassa devant eux, et il y resta jusqu&#39;aux jours de David.</p>

<p><sup class="versenum">46&nbsp;</sup>David trouva gr&acirc;ce devant Dieu, et demanda d&#39;&eacute;lever une demeure pour le Dieu de Jacob;</p>

<p><sup class="versenum">47&nbsp;</sup>et ce fut Salomon qui lui b&acirc;tit une maison.</p>

<p><sup class="versenum">48&nbsp;</sup>Mais le Tr&egrave;s Haut n&#39;habite pas dans ce qui est fait de main d&#39;homme, comme dit le proph&egrave;te:</p>

<p><sup class="versenum">49&nbsp;</sup>Le ciel est mon tr&ocirc;ne, Et la terre mon marchepied. Quelle maison me b&acirc;tirez-vous, dit le Seigneur, Ou quel sera le lieu de mon repos?</p>

<p><sup class="versenum">50&nbsp;</sup>N&#39;est-ce pas ma main qui a fait toutes ces choses?...</p>

<p><sup class="versenum">51&nbsp;</sup>Hommes au cou raide, incirconcis de coeur et d&#39;oreilles! vous vous opposez toujours au Saint Esprit. Ce que vos p&egrave;res ont &eacute;t&eacute;, vous l&#39;&ecirc;tes aussi.</p>

<p><sup class="versenum">52&nbsp;</sup>Lequel des proph&egrave;tes vos p&egrave;res n&#39;ont-ils pas pers&eacute;cut&eacute;? Ils ont tu&eacute; ceux qui annon&ccedil;aient d&#39;avance la venue du Juste, que vous avez livr&eacute; maintenant, et dont vous avez &eacute;t&eacute; les meurtriers,</p>

<p><sup class="versenum">53&nbsp;</sup>vous qui avez re&ccedil;u la loi d&#39;apr&egrave;s des commandements d&#39;anges, et qui ne l&#39;avez point gard&eacute;e!...</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/312.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 7:1-53&nbsp; </button>
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
	<li class="nobreak-final-final">Nous apprenons au sujet d&rsquo;un des sept hommes d&eacute;sign&eacute;s, &nbsp;appel&eacute; &Eacute;tienne. Le minist&egrave;re d&rsquo;&Eacute;tienne &eacute;tait de prendre soin des veuves et de g&eacute;rer les ressources de l&rsquo;&eacute;glise. En plus de cela, il annon&ccedil;ait l&rsquo;&eacute;vangile avec d&rsquo;autres Juifs qui parlent grec en visitant les synagogues. L&rsquo;Esprit a donn&eacute; le pouvoir &agrave; &Eacute;tienne d&rsquo;effectuer des miracles et de parler avec sagesse. Il s&rsquo;agit de la premi&egrave;re mention d&rsquo;un non-ap&ocirc;tre qui faisait le m&ecirc;me travail que seuls les Ap&ocirc;tres faisaient. Les Ap&ocirc;tres faisaient des disciples de la g&eacute;n&eacute;ration suivante en suivant ce qu&rsquo;ils avaient appris de J&eacute;sus. Il s&rsquo;agit d&rsquo;une r&eacute;ponse &agrave; une pri&egrave;re de J&eacute;sus &nbsp;pour les Ap&ocirc;tres et pour ceux qui croiraient suite &agrave; leur t&eacute;moignage. (<span class="popup-link" @click = "popUp('pop3')"> Jean 17:20</span>).&nbsp;

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">20&nbsp;</sup>Ce n&#39;est pas pour eux seulement que je prie, mais encore pour ceux qui croiront en moi par leur parole,</p>
<!-- end bible --></div>
Le trouble a commenc&eacute; comme un d&eacute;saccord th&eacute;ologique, puis est pass&eacute; &agrave; la calomnie (des mensonges &agrave; son sujet), &agrave; la conspiration et puis &agrave; la violence. Les fausses accusations au sujet d&rsquo;&Eacute;tienne &eacute;taient vraiment s&eacute;rieuses. En fait, elles &eacute;taient les m&ecirc;mes qui avaient &nbsp;&eacute;t&eacute; utilis&eacute;es contre J&eacute;sus. Il s&rsquo;agissait d&rsquo;une situation dangereuse, encore que le visage d&rsquo;&Eacute;tienne refl&eacute;tait la paix qui vient de la pr&eacute;sence de J&eacute;sus.Les Juifs qui parlent grec ont accus&eacute; &Eacute;tienne de parler contre le temple et contre les lois de Mo&iuml;se. En r&eacute;ponse &agrave; ces accusations, &Eacute;tienne a racont&eacute; les histoires de l&rsquo;Ancien Testament que les leaders religieux connaissaient. Il a soulign&eacute; que la pr&eacute;sence de Dieu n&rsquo;est pas li&eacute;e &agrave; un seul lieu physique. M&ecirc;me dans l&rsquo;histoire d&rsquo;Isra&euml;l, Dieu les a apparus de M&eacute;sopotamie jusqu&rsquo;en l&rsquo;&Eacute;gypte. Il a m&ecirc;me soulign&eacute; que Dieu a appel&eacute; une terre qui &eacute;tait en dehors d&rsquo;Isra&euml;l la terre sainte! Le t&eacute;moignage d&rsquo;&Eacute;tienne a montr&eacute; que Dieu &nbsp;a pris l&rsquo;initiative avec Son peuple tout au long de leur histoire: Il a parl&eacute;, Il a envoy&eacute;, Il a promis, Il a puni et Il a sauv&eacute;. Bien que Dieu avait agi, le peuple a toujours r&eacute;sist&eacute; et a m&ecirc;me tu&eacute; les proph&egrave;tes envoy&eacute;s par Dieu. Maintenant, Dieu a encore agi en envoyant J&eacute;sus. &Eacute;tienne a termin&eacute; son t&eacute;moignage en soulignant que les leaders religieux ont &eacute;t&eacute; coupables de d&eacute;sob&eacute;ir &agrave; Dieu par la trahison et le meurtre de J&eacute;sus le Messie.

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

			<td class="social" @click="share('lesson', 'La défense d\'Étienne devant le Sanhédrin: ', '/content/M2/fra/multiply3/multiply312.html')">
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