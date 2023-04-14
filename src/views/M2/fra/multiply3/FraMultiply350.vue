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
                        <div class="chapter_number ltr"><h1>50.</h1></div>
                        <div class="chapter_title ltr"><h1>Paul présente sa défense devant le roi Agrippa</h1></div>
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
	<li>Lisez ou observez Actes 25:23-26:32 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 25:23-26:32</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">23&nbsp;</sup>Le lendemain donc, Agrippa et B&eacute;r&eacute;nice vinrent en grande pompe, et entr&egrave;rent dans le lieu de l&#39;audience avec les tribuns et les principaux de la ville. Sur l&#39;ordre de Festus, Paul fut amen&eacute;.</p>

<p><sup class="versenum">24&nbsp;</sup>Alors Festus dit: Roi Agrippa, et vous tous qui &ecirc;tes pr&eacute;sents avec nous, vous voyez cet homme au sujet duquel toute la multitude des Juifs s&#39;est adress&eacute;e &agrave; moi, soit &agrave; J&eacute;rusalem, soit ici, en s&#39;&eacute;criant qu&#39;il ne devait plus vivre.</p>

<p><sup class="versenum">25&nbsp;</sup>Pour moi, ayant reconnu qu&#39;il n&#39;a rien fait qui m&eacute;rite la mort, et lui-m&ecirc;me en ayant appel&eacute; &agrave; l&#39;empereur, j&#39;ai r&eacute;solu de le faire partir.</p>

<p><sup class="versenum">26&nbsp;</sup>Je n&#39;ai rien de certain &agrave; &eacute;crire &agrave; l&#39;empereur sur son compte; c&#39;est pourquoi je l&#39;ai fait para&icirc;tre devant vous, et surtout devant toi, roi Agrippa, afin de savoir qu&#39;&eacute;crire, apr&egrave;s qu&#39;il aura &eacute;t&eacute; examin&eacute;.</p>

<p><sup class="versenum">27&nbsp;</sup>Car il me semble absurde d&#39;envoyer un prisonnier sans indiquer de quoi on l&#39;accuse.</p>

<p><sup class="versenum">1 </sup>Agrippa dit &agrave; Paul: Il t&#39;est permis de parler pour ta d&eacute;fense. Et Paul, ayant &eacute;tendu la main, se justifia en ces termes:</p>

<p><sup class="versenum">2&nbsp;</sup>Je m&#39;estime heureux, roi Agrippa, d&#39;avoir aujourd&#39;hui &agrave; me justifier devant toi de toutes les choses dont je suis accus&eacute; par les Juifs,</p>

<p><sup class="versenum">3&nbsp;</sup>car tu connais parfaitement leurs coutumes et leurs discussions. Je te prie donc de m&#39;&eacute;couter avec patience.</p>

<p><sup class="versenum">4&nbsp;</sup>Ma vie, d&egrave;s les premiers temps de ma jeunesse, est connue de tous les Juifs, puisqu&#39;elle s&#39;est pass&eacute;e &agrave; J&eacute;rusalem, au milieu de ma nation.</p>

<p><sup class="versenum">5&nbsp;</sup>Ils savent depuis longtemps, s&#39;ils veulent le d&eacute;clarer, que j&#39;ai v&eacute;cu pharisien, selon la secte la plus rigide de notre religion.</p>

<p><sup class="versenum">6&nbsp;</sup>Et maintenant, je suis mis en jugement parce que j&#39;esp&egrave;re l&#39;accomplissement de la promesse que Dieu a faite &agrave; nos p&egrave;res,</p>

<p><sup class="versenum">7&nbsp;</sup>et &agrave; laquelle aspirent nos douze tribus, qui servent Dieu continuellement nuit et jour. C&#39;est pour cette esp&eacute;rance, &ocirc; roi, que je suis accus&eacute; par des Juifs!</p>

<p><sup class="versenum">8&nbsp;</sup>Quoi! vous semble-t-il incroyable que Dieu ressuscite les morts?</p>

<p><sup class="versenum">9&nbsp;</sup>Pour moi, j&#39;avais cru devoir agir vigoureusement contre le nom de J&eacute;sus de Nazareth.</p>

<p><sup class="versenum">10&nbsp;</sup>C&#39;est ce que j&#39;ai fait &agrave; J&eacute;rusalem. J&#39;ai jet&eacute; en prison plusieurs des saints, ayant re&ccedil;u ce pouvoir des principaux sacrificateurs, et, quand on les mettait &agrave; mort, je joignais mon suffrage &agrave; celui des autres.</p>

<p><sup class="versenum">11&nbsp;</sup>je les ai souvent ch&acirc;ti&eacute;s dans toutes les synagogues, et je les for&ccedil;ais &agrave; blasph&eacute;mer. Dans mes exc&egrave;s de fureur contre eux, je les pers&eacute;cutais m&ecirc;me jusque dans les villes &eacute;trang&egrave;res.</p>

<p><sup class="versenum">12&nbsp;</sup>C&#39;est dans ce but que je me rendis &agrave; Damas, avec l&#39;autorisation et la permission des principaux sacrificateurs.</p>

<p><sup class="versenum">13&nbsp;</sup>Vers le milieu du jour, &ocirc; roi, je vis en chemin resplendir autour de moi et de mes compagnons une lumi&egrave;re venant du ciel, et dont l&#39;&eacute;clat surpassait celui du soleil.</p>

<p><sup class="versenum">14&nbsp;</sup>Nous tomb&acirc;mes tous par terre, et j&#39;entendis une voix qui me disait en langue h&eacute;bra&iuml;que: Saul, Saul, pourquoi me pers&eacute;cutes-tu? Il te serait dur de regimber contre les aiguillons.</p>

<p><sup class="versenum">15&nbsp;</sup>Je r&eacute;pondis: Qui es-tu, Seigneur? Et le Seigneur dit: Je suis J&eacute;sus que tu pers&eacute;cutes.</p>

<p><sup class="versenum">16&nbsp;</sup>Mais l&egrave;ve-toi, et tiens-toi sur tes pieds; car je te suis apparu pour t&#39;&eacute;tablir ministre et t&eacute;moin des choses que tu as vues et de celles pour lesquelles je t&#39;appara&icirc;trai.</p>

<p><sup class="versenum">17&nbsp;</sup>Je t&#39;ai choisi du milieu de ce peuple et du milieu des pa&iuml;ens, vers qui je t&#39;envoie,</p>

<p><sup class="versenum">18&nbsp;</sup>afin que tu leur ouvres les yeux, pour qu&#39;ils passent des t&eacute;n&egrave;bres &agrave; la lumi&egrave;re et de la puissance de Satan &agrave; Dieu, pour qu&#39;ils re&ccedil;oivent, par la foi en moi, le pardon des p&eacute;ch&eacute;s et l&#39;h&eacute;ritage avec les sanctifi&eacute;s.</p>

<p><sup class="versenum">19&nbsp;</sup>En cons&eacute;quence, roi Agrippa, je n&#39;ai point r&eacute;sist&eacute; &agrave; la vision c&eacute;leste:</p>

<p><sup class="versenum">20&nbsp;</sup>&agrave; ceux de Damas d&#39;abord, puis &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, et chez les pa&iuml;ens, j&#39;ai pr&ecirc;ch&eacute; la repentance et la conversion &agrave; Dieu, avec la pratique d&#39;oeuvres dignes de la repentance.</p>

<p><sup class="versenum">21&nbsp;</sup>Voil&agrave; pourquoi les Juifs se sont saisis de moi dans le temple, et ont t&acirc;ch&eacute; de me faire p&eacute;rir.</p>

<p><sup class="versenum">22&nbsp;</sup>Mais, gr&acirc;ce au secours de Dieu, j&#39;ai subsist&eacute; jusqu&#39;&agrave; ce jour, rendant t&eacute;moignage devant les petits et les grands, sans m&#39;&eacute;carter en rien de ce que les proph&egrave;tes et Mo&iuml;se ont d&eacute;clar&eacute; devoir arriver,</p>

<p><sup class="versenum">23&nbsp;</sup>savoir que le Christ souffrirait, et que, ressuscit&eacute; le premier d&#39;entre les morts, il annoncerait la lumi&egrave;re au peuple et aux nations.</p>

<p><sup class="versenum">24&nbsp;</sup>Comme il parlait ainsi pour sa justification, Festus dit &agrave; haute voix: Tu es fou, Paul! Ton grand savoir te fait d&eacute;raisonner.</p>

<p><sup class="versenum">25&nbsp;</sup>Je ne suis point fou, tr&egrave;s excellent Festus, r&eacute;pliqua Paul; ce sont, au contraire, des paroles de v&eacute;rit&eacute; et de bon sens que je prononce.</p>

<p><sup class="versenum">26&nbsp;</sup>Le roi est instruit de ces choses, et je lui en parle librement; car je suis persuad&eacute; qu&#39;il n&#39;en ignore aucune, puisque ce n&#39;est pas en cachette qu&#39;elles se sont pass&eacute;es.</p>

<p><sup class="versenum">27&nbsp;</sup>Crois-tu aux proph&egrave;tes, roi Agrippa?... Je sais que tu y crois.</p>

<p><sup class="versenum">28&nbsp;</sup>Et Agrippa dit &agrave; Paul: Tu vas bient&ocirc;t me persuader de devenir chr&eacute;tien!</p>

<p><sup class="versenum">29&nbsp;</sup>Paul r&eacute;pondit: Que ce soit bient&ocirc;t ou que ce soit tard, plaise &agrave; Dieu que non seulement toi, mais encore tous ceux qui m&#39;&eacute;coutent aujourd&#39;hui, vous deveniez tels que je suis, &agrave; l&#39;exception de ces liens!</p>

<p><sup class="versenum">30&nbsp;</sup>Le roi, le gouverneur, B&eacute;r&eacute;nice, et tous ceux qui &eacute;taient assis avec eux se lev&egrave;rent,</p>

<p><sup class="versenum">31&nbsp;</sup>et, en se retirant, ils se disaient les uns aux autres: Cet homme n&#39;a rien fait qui m&eacute;rite la mort ou la prison.</p>

<p><sup class="versenum">32&nbsp;</sup>Et Agrippa dit &agrave; Festus: Cet homme pouvait &ecirc;tre rel&acirc;ch&eacute;, s&#39;il n&#39;en e&ucirc;t pas appel&eacute; &agrave; C&eacute;sar.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/350.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 25:23-26:32&nbsp; </button>
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
	<li class="nobreak-final-final">Une fois de plus, Paul pr&eacute;sente sa d&eacute;fense. C&rsquo;est la version la plus longue enregistr&eacute;e. Paul parle devant le roi provincial juif Agrippa et le gouverneur Festus. Paul est d&eacute;j&agrave; consid&eacute;r&eacute; comme non coupable par le gouverneur qui cherchait &agrave; savoir avec clart&eacute; quoi dire &agrave; C&eacute;sar. Lisez <span class="popup-link" @click = "popUp('pop3')"> 1 Timoth&eacute;e 1: 12-16</span>.&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>Je rends gr&acirc;ces &agrave; celui qui m&#39;a fortifi&eacute;, &agrave; J&eacute;sus Christ notre Seigneur, de ce qu&#39;il m&#39;a jug&eacute; fid&egrave;le,</p>

	<p><sup class="versenum">13&nbsp;</sup>en m&#39;&eacute;tablissant dans le minist&egrave;re, moi qui &eacute;tais auparavant un blasph&eacute;mateur, un pers&eacute;cuteur, un homme violent. Mais j&#39;ai obtenu mis&eacute;ricorde, parce que j&#39;agissais par ignorance, dans l&#39;incr&eacute;dulit&eacute;;</p>

	<p><sup class="versenum">14&nbsp;</sup>et la gr&acirc;ce de notre Seigneur a surabond&eacute;, avec la foi et la charit&eacute; qui est en J&eacute;sus Christ.</p>

	<p><sup class="versenum">15&nbsp;</sup>C&#39;est une parole certaine et enti&egrave;rement digne d&#39;&ecirc;tre re&ccedil;ue, que J&eacute;sus Christ est venu dans le monde pour sauver les p&eacute;cheurs, dont je suis le premier.</p>

	<p><sup class="versenum">16&nbsp;</sup>Mais j&#39;ai obtenu mis&eacute;ricorde, afin que J&eacute;sus Christ f&icirc;t voir en moi le premier toute sa longanimit&eacute;, pour que je servisse d&#39;exemple &agrave; ceux qui croiraient en lui pour la vie &eacute;ternelle.</p>
	<!-- end bible --></div>
	Paul a admis qu&#39;il &eacute;tait exactement comme ses accusateurs avant de rencontrer J&eacute;sus. Il croyait fermement que c&#39;&eacute;tait la volont&eacute; de Dieu et qu&#39;il &eacute;tait de son devoir d&#39;arr&ecirc;ter avec violence le message de J&eacute;sus. Apparemment, Paul avait r&eacute;sist&eacute; aux incitations &agrave; accepter l&#39;&Eacute;vangile pendant cette p&eacute;riode de sa vie&nbsp;(<span class="popup-link" @click = "popUp('pop4')"> Actes 26:14</span>).

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">14&nbsp;</sup>Nous tomb&acirc;mes tous par terre, et j&#39;entendis une voix qui me disait en langue h&eacute;bra&iuml;que: Saul, Saul, pourquoi me pers&eacute;cutes-tu? Il te serait dur de regimber contre les aiguillons.</p>
	<!-- end bible --></div>
	&nbsp;J&eacute;sus a engag&eacute; ce meurtrier de Sa&uuml;l et en a fait Son serviteur afin que le monde non juif ait acc&egrave;s &agrave; l&#39;&Eacute;vangile. On nous rappelle &agrave; quel point J&eacute;sus s&#39;identifiait &eacute;troitement &agrave; ses disciples: les pers&eacute;cuter, revenait &agrave; le pers&eacute;cuter. Une fois de plus, Paul a fid&egrave;lement ob&eacute;i &agrave; son appel et a hardiment mis au d&eacute;fi les dirigeants politiques de croire en J&eacute;sus, mais ils ont rejet&eacute; l&#39;offre.</li>
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

			<td class="social" @click="share('lesson', 'Paul présente sa défense devant le roi Agrippa: ', '/content/M2/fra/multiply3/multiply350.html')">
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