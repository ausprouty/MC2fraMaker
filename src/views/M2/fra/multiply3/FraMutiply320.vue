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
                        <div class="chapter_number ltr"><h1>20.</h1></div>
                        <div class="chapter_title ltr"><h1>La Bonne Nouvelle franchit les barrières culturelles</h1></div>
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
	<li>Lisez ou observez Actes 10:34-48 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 10:34-48</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">34&nbsp;</sup>Alors Pierre, ouvrant la bouche, dit: En v&eacute;rit&eacute;, je reconnais que Dieu ne fait point acception de personnes,</p>

<p><sup class="versenum">35&nbsp;</sup>mais qu&#39;en toute nation celui qui le craint et qui pratique la justice lui est agr&eacute;able.</p>

<p><sup class="versenum">36&nbsp;</sup>Il a envoy&eacute; la parole aux fils d&#39;Isra&euml;l, en leur annon&ccedil;ant la paix par J&eacute;sus Christ, qui est le Seigneur de tous.</p>

<p><sup class="versenum">37&nbsp;</sup>Vous savez ce qui est arriv&eacute; dans toute la Jud&eacute;e, apr&egrave;s avoir commenc&eacute; en Galil&eacute;e, &agrave; la suite du bapt&ecirc;me que Jean a pr&ecirc;ch&eacute;;</p>

<p><sup class="versenum">38&nbsp;</sup>vous savez comment Dieu a oint du Saint Esprit et de force J&eacute;sus de Nazareth, qui allait de lieu en lieu faisant du bien et gu&eacute;rissant tous ceux qui &eacute;taient sous l&#39;empire du diable, car Dieu &eacute;tait avec lui.</p>

<p><sup class="versenum">39&nbsp;</sup>Nous sommes t&eacute;moins de tout ce qu&#39;il a fait dans le pays des Juifs et &agrave; J&eacute;rusalem. Ils l&#39;ont tu&eacute;, en le pendant au bois.</p>

<p><sup class="versenum">40&nbsp;</sup>Dieu l&#39;a ressuscit&eacute; le troisi&egrave;me jour, et il a permis qu&#39;il appar&ucirc;t,</p>

<p><sup class="versenum">41&nbsp;</sup>non &agrave; tout le peuple, mais aux t&eacute;moins choisis d&#39;avance par Dieu, &agrave; nous qui avons mang&eacute; et bu avec lui, apr&egrave;s qu&#39;il fut ressuscit&eacute; des morts.</p>

<p><sup class="versenum">42&nbsp;</sup>Et J&eacute;sus nous a ordonn&eacute; de pr&ecirc;cher au peuple et d&#39;attester que c&#39;est lui qui a &eacute;t&eacute; &eacute;tabli par Dieu juge des vivants et des morts.</p>

<p><sup class="versenum">43&nbsp;</sup>Tous les proph&egrave;tes rendent de lui le t&eacute;moignage que quiconque croit en lui re&ccedil;oit par son nom le pardon des p&eacute;ch&eacute;s.</p>

<p><sup class="versenum">44&nbsp;</sup>Comme Pierre pronon&ccedil;ait encore ces mots, le Saint Esprit descendit sur tous ceux qui &eacute;coutaient la parole.</p>

<p><sup class="versenum">45&nbsp;</sup>Tous les fid&egrave;les circoncis qui &eacute;taient venus avec Pierre furent &eacute;tonn&eacute;s de ce que le don du Saint Esprit &eacute;tait aussi r&eacute;pandu sur les pa&iuml;ens.</p>

<p><sup class="versenum">46&nbsp;</sup>Car ils les entendaient parler en langues et glorifier Dieu.</p>

<p><sup class="versenum">47&nbsp;</sup>Alors Pierre dit: Peut-on refuser l&#39;eau du bapt&ecirc;me &agrave; ceux qui ont re&ccedil;u le Saint Esprit aussi bien que nous?</p>

<p><sup class="versenum">48&nbsp;</sup>Et il ordonna qu&#39;ils fussent baptis&eacute;s au nom du Seigneur. Sur quoi ils le pri&egrave;rent de rester quelques jours aupr&egrave;s d&#39;eux.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/320.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 10:34-48&nbsp; </button>
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
	<li class="nobreak-final-final">Le Seigneur utilise Pierre pour apporter le salut &agrave; Corneille et &agrave; son m&eacute;nage. Cette exp&eacute;rience a enseign&eacute; &agrave; pierre et les croyants juifs qui l&rsquo;accompagne, une v&eacute;rit&eacute; th&eacute;ologique importante: le Seigneur accepte toute personne de toute nation et son offre du salut est le m&ecirc;me pour tout le monde. En renforcement &agrave; cette v&eacute;rit&eacute;, les pa&iuml;ens ont fait l&rsquo;exp&eacute;rience du don de l&rsquo;Esprit Saint de la m&ecirc;me fa&ccedil;on que les Juifs &agrave; la pentec&ocirc;te (<span class="popup-link" @click = "popUp('pop5')"> Actes 2 :4</span>,&nbsp;

	<div class="popup invisible" id="pop5"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>Et ils furent tous remplis du Saint Esprit, et se mirent &agrave; parler en d&#39;autres langues, selon que l&#39;Esprit leur donnait de s&#39;exprimer.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop6')"> Actes 10:47</span>).&nbsp;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">47&nbsp;</sup>Alors Pierre dit: Peut-on refuser l&#39;eau du bapt&ecirc;me &agrave; ceux qui ont re&ccedil;u le Saint Esprit aussi bien que nous?</p>
	<!-- end bible --></div>
	Pierre reconnait l&rsquo;acceptation des non-juifs par le Seigneur et ordonne qu&rsquo;ils &nbsp;soient imm&eacute;diatement &nbsp;baptis&eacute;s, tout comme ils l&rsquo;on fait avec les croyants Juifs. &nbsp;Pierre reste quelques jours de plus avec eux pour faire un suivi imm&eacute;diat des nouveaux croyants. Pierre a maintenant particip&eacute; &agrave; l&rsquo;implantation d&rsquo;&eacute;glises au-del&agrave; de toutes les barri&egrave;res culturelles dont &nbsp;J&eacute;sus a parl&eacute; (<span class="popup-link" @click = "popUp('pop3')"> Actes 1 :8</span>):&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">8&nbsp;</sup>Mais vous recevrez une puissance, le Saint Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&#39;aux extr&eacute;mit&eacute;s de la terre.</p>
	<!-- end bible --></div>
	&nbsp;au sein des Juifs &agrave; J&eacute;rusalem et dans toute la &nbsp;Jud&eacute;e, dans toute la &nbsp;Samarie (<span class="popup-link" @click = "popUp('pop7')"> Actes 8</span>),&nbsp;&nbsp;

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Saul avait approuv&eacute; le meurtre d&#39;&Eacute;tienne. Il y eut, ce jour-l&agrave;, une grande pers&eacute;cution contre l&#39;&Eacute;glise de J&eacute;rusalem; et tous, except&eacute; les ap&ocirc;tres, se dispers&egrave;rent dans les contr&eacute;es de la Jud&eacute;e et de la Samarie.</p>

	<p><sup class="versenum">2&nbsp;</sup>Des hommes pieux ensevelirent &Eacute;tienne, et le pleur&egrave;rent &agrave; grand bruit.</p>

	<p><sup class="versenum">3&nbsp;</sup>Saul, de son c&ocirc;t&eacute;, ravageait l&#39;&Eacute;glise; p&eacute;n&eacute;trant dans les maisons, il en arrachait hommes et femmes, et les faisait jeter en prison.</p>

	<p><sup class="versenum">4&nbsp;</sup>Ceux qui avaient &eacute;t&eacute; dispers&eacute;s allaient de lieu en lieu, annon&ccedil;ant la bonne nouvelle de la parole.</p>

	<p><sup class="versenum">5&nbsp;</sup>Philippe, &eacute;tant descendu dans la ville de Samarie, y pr&ecirc;cha le Christ.</p>

	<p><sup class="versenum">6&nbsp;</sup>Les foules tout enti&egrave;res &eacute;taient attentives &agrave; ce que disait Philippe, lorsqu&#39;elles apprirent et virent les miracles qu&#39;il faisait.</p>

	<p><sup class="versenum">7&nbsp;</sup>Car des esprits impurs sortirent de plusieurs d&eacute;moniaques, en poussant de grands cris, et beaucoup de paralytiques et de boiteux furent gu&eacute;ris.</p>

	<p><sup class="versenum">8&nbsp;</sup>Et il y eut une grande joie dans cette ville.</p>

	<p><sup class="versenum">9&nbsp;</sup>Il y avait auparavant dans la ville un homme nomm&eacute; Simon, qui, se donnant pour un personnage important, exer&ccedil;ait la magie et provoquait l&#39;&eacute;tonnement du peuple de la Samarie.</p>

	<p><sup class="versenum">10&nbsp;</sup>Tous, depuis le plus petit jusqu&#39;au plus grand, l&#39;&eacute;coutaient attentivement, et disaient: Celui-ci est la puissance de Dieu, celle qui s&#39;appelle la grande.</p>

	<p><sup class="versenum">11&nbsp;</sup>Ils l&#39;&eacute;coutaient attentivement, parce qu&#39;il les avait longtemps &eacute;tonn&eacute;s par ses actes de magie.</p>

	<p><sup class="versenum">12&nbsp;</sup>Mais, quand ils eurent cru &agrave; Philippe, qui leur annon&ccedil;ait la bonne nouvelle du royaume de Dieu et du nom de J&eacute;sus Christ, hommes et femmes se firent baptiser.</p>

	<p><sup class="versenum">13&nbsp;</sup>Simon lui-m&ecirc;me crut, et, apr&egrave;s avoir &eacute;t&eacute; baptis&eacute;, il ne quittait plus Philippe, et il voyait avec &eacute;tonnement les miracles et les grands prodiges qui s&#39;op&eacute;raient.</p>

	<p><sup class="versenum">14&nbsp;</sup>Les ap&ocirc;tres, qui &eacute;taient &agrave; J&eacute;rusalem, ayant appris que la Samarie avait re&ccedil;u la parole de Dieu, y envoy&egrave;rent Pierre et Jean.</p>

	<p><sup class="versenum">15&nbsp;</sup>Ceux-ci, arriv&eacute;s chez les Samaritains, pri&egrave;rent pour eux, afin qu&#39;ils re&ccedil;ussent le Saint Esprit.</p>

	<p><sup class="versenum">16&nbsp;</sup>Car il n&#39;&eacute;tait encore descendu sur aucun d&#39;eux; ils avaient seulement &eacute;t&eacute; baptis&eacute;s au nom du Seigneur J&eacute;sus.</p>

	<p><sup class="versenum">17&nbsp;</sup>Alors Pierre et Jean leur impos&egrave;rent les mains, et ils re&ccedil;urent le Saint Esprit.</p>

	<p><sup class="versenum">18&nbsp;</sup>Lorsque Simon vit que le Saint Esprit &eacute;tait donn&eacute; par l&#39;imposition des mains des ap&ocirc;tres, il leur offrit de l&#39;argent,</p>

	<p><sup class="versenum">19&nbsp;</sup>en disant: Accordez-moi aussi ce pouvoir, afin que celui &agrave; qui j&#39;imposerai les mains re&ccedil;oive le Saint Esprit.</p>

	<p><sup class="versenum">20&nbsp;</sup>Mais Pierre lui dit: Que ton argent p&eacute;risse avec toi, puisque tu as cru que le don de Dieu s&#39;acqu&eacute;rait &agrave; prix d&#39;argent!</p>

	<p><sup class="versenum">21&nbsp;</sup>Il n&#39;y a pour toi ni part ni lot dans cette affaire, car ton coeur n&#39;est pas droit devant Dieu.</p>

	<p><sup class="versenum">22&nbsp;</sup>Repens-toi donc de ta m&eacute;chancet&eacute;, et prie le Seigneur pour que la pens&eacute;e de ton coeur te soit pardonn&eacute;e, s&#39;il est possible;</p>

	<p><sup class="versenum">23&nbsp;</sup>car je vois que tu es dans un fiel amer et dans les liens de l&#39;iniquit&eacute;.</p>

	<p><sup class="versenum">24&nbsp;</sup>Simon r&eacute;pondit: Priez vous-m&ecirc;mes le Seigneur pour moi, afin qu&#39;il ne m&#39;arrive rien de ce que vous avez dit.</p>

	<p><sup class="versenum">25&nbsp;</sup>Apr&egrave;s avoir rendu t&eacute;moignage &agrave; la parole du Seigneur, et apr&egrave;s l&#39;avoir pr&ecirc;ch&eacute;e, Pierre et Jean retourn&egrave;rent &agrave; J&eacute;rusalem, en annon&ccedil;ant la bonne nouvelle dans plusieurs villages des Samaritains.</p>

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
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	et maintenant au sein des pa&iuml;ens (<span class="popup-link" @click = "popUp('pop4')"> Actes 10</span>).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Il y avait &agrave; C&eacute;sar&eacute;e un homme nomm&eacute; Corneille, centenier dans la cohorte dite italienne.</p>

	<p><sup class="versenum">2&nbsp;</sup>Cet homme &eacute;tait pieux et craignait Dieu, avec toute sa maison; il faisait beaucoup d&#39;aum&ocirc;nes au peuple, et priait Dieu continuellement.</p>

	<p><sup class="versenum">3&nbsp;</sup>Vers la neuvi&egrave;me heure du jour, il vit clairement dans une vision un ange de Dieu qui entra chez lui, et qui lui dit: Corneille!</p>

	<p><sup class="versenum">4&nbsp;</sup>Les regards fix&eacute;s sur lui, et saisi d&#39;effroi, il r&eacute;pondit: Qu&#39;est-ce, Seigneur? Et l&#39;ange lui dit: Tes pri&egrave;res et tes aum&ocirc;nes sont mont&eacute;es devant Dieu, et il s&#39;en est souvenu.</p>

	<p><sup class="versenum">5&nbsp;</sup>Envoie maintenant des hommes &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre;</p>

	<p><sup class="versenum">6&nbsp;</sup>il est log&eacute; chez un certain Simon, corroyeur, dont la maison est pr&egrave;s de la mer.</p>

	<p><sup class="versenum">7&nbsp;</sup>D&egrave;s que l&#39;ange qui lui avait parl&eacute; fut parti, Corneille appela deux de ses serviteurs, et un soldat pieux d&#39;entre ceux qui &eacute;taient attach&eacute;s &agrave; sa personne;</p>

	<p><sup class="versenum">8&nbsp;</sup>et, apr&egrave;s leur avoir tout racont&eacute;, il les envoya &agrave; Jopp&eacute;.</p>

	<p><sup class="versenum">9&nbsp;</sup>Le lendemain, comme ils &eacute;taient en route, et qu&#39;ils approchaient de la ville, Pierre monta sur le toit, vers la sixi&egrave;me heure, pour prier.</p>

	<p><sup class="versenum">10&nbsp;</sup>Il eut faim, et il voulut manger. Pendant qu&#39;on lui pr&eacute;parait &agrave; manger, il tomba en extase.</p>

	<p><sup class="versenum">11&nbsp;</sup>Il vit le ciel ouvert, et un objet semblable &agrave; une grande nappe attach&eacute;e par les quatre coins, qui descendait et s&#39;abaissait vers la terre,</p>

	<p><sup class="versenum">12&nbsp;</sup>et o&ugrave; se trouvaient tous les quadrup&egrave;des et les reptiles de la terre et les oiseaux du ciel.</p>

	<p><sup class="versenum">13&nbsp;</sup>Et une voix lui dit: L&egrave;ve-toi, Pierre, tue et mange.</p>

	<p><sup class="versenum">14&nbsp;</sup>Mais Pierre dit: Non, Seigneur, car je n&#39;ai jamais rien mang&eacute; de souill&eacute; ni d&#39;impur.</p>

	<p><sup class="versenum">15&nbsp;</sup>Et pour la seconde fois la voix se fit encore entendre &agrave; lui: Ce que Dieu a d&eacute;clar&eacute; pur, ne le regarde pas comme souill&eacute;.</p>

	<p><sup class="versenum">16&nbsp;</sup>Cela arriva jusqu&#39;&agrave; trois fois; et aussit&ocirc;t apr&egrave;s, l&#39;objet fut retir&eacute; dans le ciel.</p>

	<p><sup class="versenum">17&nbsp;</sup>Tandis que Pierre ne savait en lui-m&ecirc;me que penser du sens de la vision qu&#39;il avait eue, voici, les hommes envoy&eacute;s par Corneille, s&#39;&eacute;tant inform&eacute;s de la maison de Simon, se pr&eacute;sent&egrave;rent &agrave; la porte,</p>

	<p><sup class="versenum">18&nbsp;</sup>et demand&egrave;rent &agrave; haute voix si c&#39;&eacute;tait l&agrave; que logeait Simon, surnomm&eacute; Pierre.</p>

	<p><sup class="versenum">19&nbsp;</sup>Et comme Pierre &eacute;tait &agrave; r&eacute;fl&eacute;chir sur la vision, l&#39;Esprit lui dit: Voici, trois hommes te demandent;</p>

	<p><sup class="versenum">20&nbsp;</sup>l&egrave;ve-toi, descends, et pars avec eux sans h&eacute;siter, car c&#39;est moi qui les ai envoy&eacute;s.</p>

	<p><sup class="versenum">21&nbsp;</sup>Pierre donc descendit, et il dit &agrave; ces hommes: Voici, je suis celui que vous cherchez; quel est le motif qui vous am&egrave;ne?</p>

	<p><sup class="versenum">22&nbsp;</sup>Ils r&eacute;pondirent: Corneille, centenier, homme juste et craignant Dieu, et de qui toute la nation des Juifs rend un bon t&eacute;moignage, a &eacute;t&eacute; divinement averti par un saint ange de te faire venir dans sa maison et d&#39;entendre tes paroles.</p>

	<p><sup class="versenum">23&nbsp;</sup>Pierre donc les fit entrer, et les logea. Le lendemain, il se leva, et partit avec eux. Quelques-uns des fr&egrave;res de Jopp&eacute; l&#39;accompagn&egrave;rent.</p>

	<p><sup class="versenum">24&nbsp;</sup>Ils arriv&egrave;rent &agrave; C&eacute;sar&eacute;e le jour suivant. Corneille les attendait, et avait invit&eacute; ses parents et ses amis intimes.</p>

	<p><sup class="versenum">25&nbsp;</sup>Lorsque Pierre entra, Corneille, qui &eacute;tait all&eacute; au-devant de lui, tomba &agrave; ses pieds et se prosterna.</p>

	<p><sup class="versenum">26&nbsp;</sup>Mais Pierre le releva, en disant: L&egrave;ve-toi; moi aussi, je suis un homme.</p>

	<p><sup class="versenum">27&nbsp;</sup>Et conversant avec lui, il entra, et trouva beaucoup de personnes r&eacute;unies.</p>

	<p><sup class="versenum">28&nbsp;</sup>Vous savez, leur dit-il, qu&#39;il est d&eacute;fendu &agrave; un Juif de se lier avec un &eacute;tranger ou d&#39;entrer chez lui; mais Dieu m&#39;a appris &agrave; ne regarder aucun homme comme souill&eacute; et impur.</p>

	<p><sup class="versenum">29&nbsp;</sup>C&#39;est pourquoi je n&#39;ai pas eu d&#39;objection &agrave; venir, puisque vous m&#39;avez appel&eacute;; je vous demande donc pour quel motif vous m&#39;avez envoy&eacute; chercher.</p>

	<p><sup class="versenum">30&nbsp;</sup>Corneille dit: Il y a quatre jours, &agrave; cette heure-ci, je priais dans ma maison &agrave; la neuvi&egrave;me heure; et voici, un homme v&ecirc;tu d&#39;un habit &eacute;clatant se pr&eacute;senta devant moi, et dit:</p>

	<p><sup class="versenum">31&nbsp;</sup>Corneille, ta pri&egrave;re a &eacute;t&eacute; exauc&eacute;e, et Dieu s&#39;est souvenu de tes aum&ocirc;nes.</p>

	<p><sup class="versenum">32&nbsp;</sup>Envoie donc &agrave; Jopp&eacute;, et fais venir Simon, surnomm&eacute; Pierre; il est log&eacute; dans la maison de Simon, corroyeur, pr&egrave;s de la mer.</p>

	<p><sup class="versenum">33&nbsp;</sup>Aussit&ocirc;t j&#39;ai envoy&eacute; vers toi, et tu as bien fait de venir. Maintenant donc nous sommes tous devant Dieu, pour entendre tout ce que le Seigneur t&#39;a ordonn&eacute; de nous dire.</p>

	<p><sup class="versenum">34&nbsp;</sup>Alors Pierre, ouvrant la bouche, dit: En v&eacute;rit&eacute;, je reconnais que Dieu ne fait point acception de personnes,</p>

	<p><sup class="versenum">35&nbsp;</sup>mais qu&#39;en toute nation celui qui le craint et qui pratique la justice lui est agr&eacute;able.</p>

	<p><sup class="versenum">36&nbsp;</sup>Il a envoy&eacute; la parole aux fils d&#39;Isra&euml;l, en leur annon&ccedil;ant la paix par J&eacute;sus Christ, qui est le Seigneur de tous.</p>

	<p><sup class="versenum">37&nbsp;</sup>Vous savez ce qui est arriv&eacute; dans toute la Jud&eacute;e, apr&egrave;s avoir commenc&eacute; en Galil&eacute;e, &agrave; la suite du bapt&ecirc;me que Jean a pr&ecirc;ch&eacute;;</p>

	<p><sup class="versenum">38&nbsp;</sup>vous savez comment Dieu a oint du Saint Esprit et de force J&eacute;sus de Nazareth, qui allait de lieu en lieu faisant du bien et gu&eacute;rissant tous ceux qui &eacute;taient sous l&#39;empire du diable, car Dieu &eacute;tait avec lui.</p>

	<p><sup class="versenum">39&nbsp;</sup>Nous sommes t&eacute;moins de tout ce qu&#39;il a fait dans le pays des Juifs et &agrave; J&eacute;rusalem. Ils l&#39;ont tu&eacute;, en le pendant au bois.</p>

	<p><sup class="versenum">40&nbsp;</sup>Dieu l&#39;a ressuscit&eacute; le troisi&egrave;me jour, et il a permis qu&#39;il appar&ucirc;t,</p>

	<p><sup class="versenum">41&nbsp;</sup>non &agrave; tout le peuple, mais aux t&eacute;moins choisis d&#39;avance par Dieu, &agrave; nous qui avons mang&eacute; et bu avec lui, apr&egrave;s qu&#39;il fut ressuscit&eacute; des morts.</p>

	<p><sup class="versenum">42&nbsp;</sup>Et J&eacute;sus nous a ordonn&eacute; de pr&ecirc;cher au peuple et d&#39;attester que c&#39;est lui qui a &eacute;t&eacute; &eacute;tabli par Dieu juge des vivants et des morts.</p>

	<p><sup class="versenum">43&nbsp;</sup>Tous les proph&egrave;tes rendent de lui le t&eacute;moignage que quiconque croit en lui re&ccedil;oit par son nom le pardon des p&eacute;ch&eacute;s.</p>

	<p><sup class="versenum">44&nbsp;</sup>Comme Pierre pronon&ccedil;ait encore ces mots, le Saint Esprit descendit sur tous ceux qui &eacute;coutaient la parole.</p>

	<p><sup class="versenum">45&nbsp;</sup>Tous les fid&egrave;les circoncis qui &eacute;taient venus avec Pierre furent &eacute;tonn&eacute;s de ce que le don du Saint Esprit &eacute;tait aussi r&eacute;pandu sur les pa&iuml;ens.</p>

	<p><sup class="versenum">46&nbsp;</sup>Car ils les entendaient parler en langues et glorifier Dieu.</p>

	<p><sup class="versenum">47&nbsp;</sup>Alors Pierre dit: Peut-on refuser l&#39;eau du bapt&ecirc;me &agrave; ceux qui ont re&ccedil;u le Saint Esprit aussi bien que nous?</p>

	<p><sup class="versenum">48&nbsp;</sup>Et il ordonna qu&#39;ils fussent baptis&eacute;s au nom du Seigneur. Sur quoi ils le pri&egrave;rent de rester quelques jours aupr&egrave;s d&#39;eux.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	Les portes de toutes les barri&egrave;res culturelles sont maintenant d&eacute;verrouill&eacute;es pour l&rsquo;expansion du royaume.</li>
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

			<td class="social" @click="share('lesson', 'La Bonne Nouvelle franchit les barrières culturelles: ', '/content/M2/fra/multiply3/mutiply320.html')">
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