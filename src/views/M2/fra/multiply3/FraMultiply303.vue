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
                        <div class="chapter_number ltr"><h1>3.</h1></div>
                        <div class="chapter_title ltr"><h1>Le Saint-Esprit est venu le jour de la Pentecôte</h1></div>
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
	<li>Lisez ou observez Actes 2:1-13 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 2:1-13</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Le jour de la Pentec&ocirc;te, ils &eacute;taient tous ensemble dans le m&ecirc;me lieu.</p>

<p><sup class="versenum">2&nbsp;</sup>Tout &agrave; coup il vint du ciel un bruit comme celui d&#39;un vent imp&eacute;tueux, et il remplit toute la maison o&ugrave; ils &eacute;taient assis.</p>

<p><sup class="versenum">3&nbsp;</sup>Des langues, semblables &agrave; des langues de feu, leur apparurent, s&eacute;par&eacute;es les unes des autres, et se pos&egrave;rent sur chacun d&#39;eux.</p>

<p><sup class="versenum">4&nbsp;</sup>Et ils furent tous remplis du Saint Esprit, et se mirent &agrave; parler en d&#39;autres langues, selon que l&#39;Esprit leur donnait de s&#39;exprimer.</p>

<p><sup class="versenum">5&nbsp;</sup>Or, il y avait en s&eacute;jour &agrave; J&eacute;rusalem des Juifs, hommes pieux, de toutes les nations qui sont sous le ciel.</p>

<p><sup class="versenum">6&nbsp;</sup>Au bruit qui eut lieu, la multitude accourut, et elle fut confondue parce que chacun les entendait parler dans sa propre langue.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils &eacute;taient tous dans l&#39;&eacute;tonnement et la surprise, et ils se disaient les uns aux autres: Voici, ces gens qui parlent ne sont-ils pas tous Galil&eacute;ens?</p>

<p><sup class="versenum">8&nbsp;</sup>Et comment les entendons-nous dans notre propre langue &agrave; chacun, dans notre langue maternelle?</p>

<p><sup class="versenum">9&nbsp;</sup>Parthes, M&egrave;des, &Eacute;lamites, ceux qui habitent la M&eacute;sopotamie, la Jud&eacute;e, la Cappadoce, le Pont, l&#39;Asie,</p>

<p><sup class="versenum">10&nbsp;</sup>la Phrygie, la Pamphylie, l&#39;&Eacute;gypte, le territoire de la Libye voisine de Cyr&egrave;ne, et ceux qui sont venus de Rome, Juifs et pros&eacute;lytes,</p>

<p><sup class="versenum">11&nbsp;</sup>Cr&eacute;tois et Arabes, comment les entendons-nous parler dans nos langues des merveilles de Dieu?</p>

<p><sup class="versenum">12&nbsp;</sup>Ils &eacute;taient tous dans l&#39;&eacute;tonnement, et, ne sachant que penser, ils se disaient les uns aux autres: Que veut dire ceci?</p>

<p><sup class="versenum">13&nbsp;</sup>Mais d&#39;autres se moquaient, et disaient: Ils sont pleins de vin doux.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/303.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 2:1-13&nbsp; </button>
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

<p>La Pentec&ocirc;te &eacute;tait l&#39;une des trois principales f&ecirc;tes annuelles juives &agrave; laquelle assistaient des p&egrave;lerins juifs venus de toutes parts du monde romain. Elle a lieu 50 jours apr&egrave;s la f&ecirc;te de la P&acirc;que et est l&#39;anniversaire de la r&eacute;ception de la Loi de Dieu par Mo&iuml;se dans l&#39;Ancien Testament (<span class="popup-link" @click = "popUp('pop3')"> Exode 20</span>).</p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">1 </sup>Alors Dieu pronon&ccedil;a toutes ces paroles, en disant:</p>

<p><sup class="versenum">2&nbsp;</sup>Je suis l&#39;&Eacute;ternel, ton Dieu, qui t&#39;ai fait sortir du pays d&#39;&Eacute;gypte, de la maison de servitude.</p>

<p><sup class="versenum">3&nbsp;</sup>Tu n&#39;auras pas d&#39;autres dieux devant ma face.</p>

<p><sup class="versenum">4&nbsp;</sup>Tu ne te feras point d&#39;image taill&eacute;e, ni de repr&eacute;sentation quelconque des choses qui sont en haut dans les cieux, qui sont en bas sur la terre, et qui sont dans les eaux plus bas que la terre.</p>

<p><sup class="versenum">5&nbsp;</sup>Tu ne te prosterneras point devant elles, et tu ne les serviras point; car moi, l&#39;&Eacute;ternel, ton Dieu, je suis un Dieu jaloux, qui punis l&#39;iniquit&eacute; des p&egrave;res sur les enfants jusqu&#39;&agrave; la troisi&egrave;me et la quatri&egrave;me g&eacute;n&eacute;ration de ceux qui me ha&iuml;ssent,</p>

<p><sup class="versenum">6&nbsp;</sup>et qui fais mis&eacute;ricorde jusqu&#39;en mille g&eacute;n&eacute;rations &agrave; ceux qui m&#39;aiment et qui gardent mes commandements.</p>

<p><sup class="versenum">7&nbsp;</sup>Tu ne prendras point le nom de l&#39;&Eacute;ternel, ton Dieu, en vain; car l&#39;&Eacute;ternel ne laissera point impuni celui qui prendra son nom en vain.</p>

<p><sup class="versenum">8&nbsp;</sup>Souviens-toi du jour du repos, pour le sanctifier.</p>

<p><sup class="versenum">9&nbsp;</sup>Tu travailleras six jours, et tu feras tout ton ouvrage.</p>

<p><sup class="versenum">10&nbsp;</sup>Mais le septi&egrave;me jour est le jour du repos de l&#39;&Eacute;ternel, ton Dieu: tu ne feras aucun ouvrage, ni toi, ni ton fils, ni ta fille, ni ton serviteur, ni ta servante, ni ton b&eacute;tail, ni l&#39;&eacute;tranger qui est dans tes portes.</p>

<p><sup class="versenum">11&nbsp;</sup>Car en six jours l&#39;&Eacute;ternel a fait les cieux, la terre et la mer, et tout ce qui y est contenu, et il s&#39;est repos&eacute; le septi&egrave;me jour: c&#39;est pourquoi l&#39;&Eacute;ternel a b&eacute;ni le jour du repos et l&#39;a sanctifi&eacute;.</p>

<p><sup class="versenum">12&nbsp;</sup>Honore ton p&egrave;re et ta m&egrave;re, afin que tes jours se prolongent dans le pays que l&#39;&Eacute;ternel, ton Dieu, te donne.</p>

<p><sup class="versenum">13&nbsp;</sup>Tu ne tueras point.</p>

<p><sup class="versenum">14&nbsp;</sup>Tu ne commettras point d&#39;adult&egrave;re.</p>

<p><sup class="versenum">15&nbsp;</sup>Tu ne d&eacute;roberas point.</p>

<p><sup class="versenum">16&nbsp;</sup>Tu ne porteras point de faux t&eacute;moignage contre ton prochain.</p>

<p><sup class="versenum">17&nbsp;</sup>Tu ne convoiteras point la maison de ton prochain; tu ne convoiteras point la femme de ton prochain, ni son serviteur, ni sa servante, ni son boeuf, ni son &acirc;ne, ni aucune chose qui appartienne &agrave; ton prochain.</p>

<p><sup class="versenum">18&nbsp;</sup>Tout le peuple entendait les tonnerres et le son de la trompette; il voyait les flammes de la montagne fumante. A ce spectacle, le peuple tremblait, et se tenait dans l&#39;&eacute;loignement.</p>

<p><sup class="versenum">19&nbsp;</sup>Ils dirent &agrave; Mo&iuml;se: Parle-nous toi-m&ecirc;me, et nous &eacute;couterons; mais que Dieu ne nous parle point, de peur que nous ne mourions.</p>

<p><sup class="versenum">20&nbsp;</sup>Mo&iuml;se dit au peuple: Ne vous effrayez pas; car c&#39;est pour vous mettre &agrave; l&#39;&eacute;preuve que Dieu est venu, et c&#39;est pour que vous ayez sa crainte devant les yeux, afin que vous ne p&eacute;chiez point.</p>

<p><sup class="versenum">21&nbsp;</sup>Le peuple restait dans l&#39;&eacute;loignement; mais Mo&iuml;se s&#39;approcha de la nu&eacute;e o&ugrave; &eacute;tait Dieu.</p>

<p><sup class="versenum">22&nbsp;</sup>L&#39;&Eacute;ternel dit &agrave; Mo&iuml;se: Tu parleras ainsi aux enfants d&#39;Isra&euml;l: Vous avez vu que je vous ai parl&eacute; depuis les cieux.</p>

<p><sup class="versenum">23&nbsp;</sup>Vous ne ferez point des dieux d&#39;argent et des dieux d&#39;or, pour me les associer; vous ne vous en ferez point.</p>

<p><sup class="versenum">24&nbsp;</sup>Tu m&#39;&eacute;l&egrave;veras un autel de terre, sur lequel tu offriras tes holocaustes et tes sacrifices d&#39;actions de gr&acirc;ces, tes brebis et tes boeufs. Partout o&ugrave; je rappellerai mon nom, je viendrai &agrave; toi, et je te b&eacute;nirai.</p>

<p><sup class="versenum">25&nbsp;</sup>Si tu m&#39;&eacute;l&egrave;ves un autel de pierre, tu ne le b&acirc;tiras point en pierres taill&eacute;es; car en passant ton ciseau sur la pierre, tu la profanerais.</p>

<p><sup class="versenum">26&nbsp;</sup>Tu ne monteras point &agrave; mon autel par des degr&eacute;s, afin que ta nudit&eacute; ne soit pas d&eacute;couverte.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible --></div>
120 hommes et femmes s&rsquo;&eacute;taient assembl&eacute;s lorsque l&#39;Esprit est venu. La nuit o&ugrave; J&eacute;sus a &eacute;t&eacute; arr&ecirc;t&eacute;, il a enseign&eacute; aux disciples que l&#39;Esprit qui vient, sera un autre consolateur qui demeurera en eux (<span class="popup-link" @click = "popUp('pop4')"> Jean 14: 16-17</span>)

<div class="popup invisible" id="pop4"><!-- begin bible -->
<p><sup class="versenum">16&nbsp;</sup>Et moi, je prierai le P&egrave;re, et il vous donnera un autre consolateur, afin qu&#39;il demeure &eacute;ternellement avec vous,</p>

<p><sup class="versenum">17&nbsp;</sup>l&#39;Esprit de v&eacute;rit&eacute;, que le monde ne peut recevoir, parce qu&#39;il ne le voit point et ne le conna&icirc;t point; mais vous, vous le connaissez, car il demeure avec vous, et il sera en vous.</p>
<!-- end bible --></div>
Cette nouvelle relation avec le Saint-Esprit a &eacute;t&eacute; promise des centaines d&#39;ann&eacute;es plus t&ocirc;t par des proph&egrave;tes comme &Eacute;z&eacute;chiel. Lisez <span class="popup-link" @click = "popUp('pop7')"> &Eacute;z&eacute;chiel 36:26-27</span>.&nbsp;

<div class="popup invisible" id="pop7"><!-- begin bible -->
<p><sup class="versenum">26&nbsp;</sup>Je vous donnerai un coeur nouveau, et je mettrai en vous un esprit nouveau; j&#39;&ocirc;terai de votre corps le coeur de pierre, et je vous donnerai un coeur de chair.</p>

<p><sup class="versenum">27&nbsp;</sup>Je mettrai mon esprit en vous, et je ferai en sorte que vous suiviez mes ordonnances, et que vous observiez et pratiquiez mes lois.</p>
<!-- end bible --></div>

<div class="popup invisible" id="pop7">&nbsp;</div>
L&#39;Esprit a &eacute;t&eacute; envoy&eacute; pour consoler, enseigner, conduire, convaincre du p&eacute;ch&eacute;, produire du fruit et habiliter les disciples &agrave; continuer l&#39;&oelig;uvre pour laquelle J&eacute;sus les avait form&eacute;s (<span class="popup-link" @click = "popUp('pop6')"> Jean 14-15</span>).

<div class="popup invisible" id="pop6"><!-- begin bible -->
<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">1 </sup>Que votre coeur ne se trouble point. Croyez en Dieu, et croyez en moi.</p>

<p><sup class="versenum">2&nbsp;</sup>Il y a plusieurs demeures dans la maison de mon P&egrave;re. Si cela n&#39;&eacute;tait pas, je vous l&#39;aurais dit. Je vais vous pr&eacute;parer une place.</p>

<p><sup class="versenum">3&nbsp;</sup>Et, lorsque je m&#39;en serai all&eacute;, et que je vous aurai pr&eacute;par&eacute; une place, je reviendrai, et je vous prendrai avec moi, afin que l&agrave; o&ugrave; je suis vous y soyez aussi.</p>

<p><sup class="versenum">4&nbsp;</sup>Vous savez o&ugrave; je vais, et vous en savez le chemin.</p>

<p><sup class="versenum">5&nbsp;</sup>Thomas lui dit: Seigneur, nous ne savons o&ugrave; tu vas; comment pouvons-nous en savoir le chemin?</p>

<p><sup class="versenum">6&nbsp;</sup>J&eacute;sus lui dit: Je suis le chemin, la v&eacute;rit&eacute;, et la vie. Nul ne vient au P&egrave;re que par moi.</p>

<p><sup class="versenum">7&nbsp;</sup>Si vous me connaissiez, vous conna&icirc;triez aussi mon P&egrave;re. Et d&egrave;s maintenant vous le connaissez, et vous l&#39;avez vu.</p>

<p><sup class="versenum">8&nbsp;</sup>Philippe lui dit: Seigneur, montre-nous le P&egrave;re, et cela nous suffit.</p>

<p><sup class="versenum">9&nbsp;</sup>J&eacute;sus lui dit: Il y a si longtemps que je suis avec vous, et tu ne m&#39;as pas connu, Philippe! Celui qui m&#39;a vu a vu le P&egrave;re; comment dis-tu: Montre-nous le P&egrave;re?</p>

<p><sup class="versenum">10&nbsp;</sup>Ne crois-tu pas que je suis dans le P&egrave;re, et que le P&egrave;re est en moi? Les paroles que je vous dis, je ne les dis pas de moi-m&ecirc;me; et le P&egrave;re qui demeure en moi, c&#39;est lui qui fait les oeuvres.</p>

<p><sup class="versenum">11&nbsp;</sup>Croyez-moi, je suis dans le P&egrave;re, et le P&egrave;re est en moi; croyez du moins &agrave; cause de ces oeuvres.</p>

<p><sup class="versenum">12&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les oeuvres que je fais, et il en fera de plus grandes, parce que je m&#39;en vais au P&egrave;re;</p>

<p><sup class="versenum">13&nbsp;</sup>et tout ce que vous demanderez en mon nom, je le ferai, afin que le P&egrave;re soit glorifi&eacute; dans le Fils.</p>

<p><sup class="versenum">14&nbsp;</sup>Si vous demandez quelque chose en mon nom, je le ferai.</p>

<p><sup class="versenum">15&nbsp;</sup>Si vous m&#39;aimez, gardez mes commandements.</p>

<p><sup class="versenum">16&nbsp;</sup>Et moi, je prierai le P&egrave;re, et il vous donnera un autre consolateur, afin qu&#39;il demeure &eacute;ternellement avec vous,</p>

<p><sup class="versenum">17&nbsp;</sup>l&#39;Esprit de v&eacute;rit&eacute;, que le monde ne peut recevoir, parce qu&#39;il ne le voit point et ne le conna&icirc;t point; mais vous, vous le connaissez, car il demeure avec vous, et il sera en vous.</p>

<p><sup class="versenum">18&nbsp;</sup>Je ne vous laisserai pas orphelins, je viendrai &agrave; vous.</p>

<p><sup class="versenum">19&nbsp;</sup>Encore un peu de temps, et le monde ne me verra plus; mais vous, vous me verrez, car je vis, et vous vivrez aussi.</p>

<p><sup class="versenum">20&nbsp;</sup>En ce jour-l&agrave;, vous conna&icirc;trez que je suis en mon P&egrave;re, que vous &ecirc;tes en moi, et que je suis en vous.</p>

<p><sup class="versenum">21&nbsp;</sup>Celui qui a mes commandements et qui les garde, c&#39;est celui qui m&#39;aime; et celui qui m&#39;aime sera aim&eacute; de mon P&egrave;re, je l&#39;aimerai, et je me ferai conna&icirc;tre &agrave; lui.</p>

<p><sup class="versenum">22&nbsp;</sup>Jude, non pas l&#39;Iscariot, lui dit: Seigneur, d&#39;o&ugrave; vient que tu te feras conna&icirc;tre &agrave; nous, et non au monde?</p>

<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Si quelqu&#39;un m&#39;aime, il gardera ma parole, et mon P&egrave;re l&#39;aimera; nous viendrons &agrave; lui, et nous ferons notre demeure chez lui.</p>

<p><sup class="versenum">24&nbsp;</sup>Celui qui ne m&#39;aime pas ne garde point mes paroles. Et la parole que vous entendez n&#39;est pas de moi, mais du P&egrave;re qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">25&nbsp;</sup>Je vous ai dit ces choses pendant que je demeure avec vous.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais le consolateur, l&#39;Esprit Saint, que le P&egrave;re enverra en mon nom, vous enseignera toutes choses, et vous rappellera tout ce que je vous ai dit.</p>

<p><sup class="versenum">27&nbsp;</sup>Je vous laisse la paix, je vous donne ma paix. Je ne vous donne pas comme le monde donne. Que votre coeur ne se trouble point, et ne s&#39;alarme point.</p>

<p><sup class="versenum">28&nbsp;</sup>Vous avez entendu que je vous ai dit: Je m&#39;en vais, et je reviens vers vous. Si vous m&#39;aimiez, vous vous r&eacute;jouiriez de ce que je vais au P&egrave;re; car le P&egrave;re est plus grand que moi.</p>

<p><sup class="versenum">29&nbsp;</sup>Et maintenant je vous ai dit ces choses avant qu&#39;elles arrivent, afin que, lorsqu&#39;elles arriveront, vous croyiez.</p>

<p><sup class="versenum">30&nbsp;</sup>Je ne parlerai plus gu&egrave;re avec vous; car le prince du monde vient. Il n&#39;a rien en moi;</p>

<p><sup class="versenum">31&nbsp;</sup>mais afin que le monde sache que j&#39;aime le P&egrave;re, et que j&#39;agis selon l&#39;ordre que le P&egrave;re m&#39;a donn&eacute;, levez-vous, partons d&#39;ici.</p>

<p><sup class="versenum">1 </sup>Je suis le vrai cep, et mon P&egrave;re est le vigneron.</p>

<p><sup class="versenum">2&nbsp;</sup>Tout sarment qui est en moi et qui ne porte pas de fruit, il le retranche; et tout sarment qui porte du fruit, il l&#39;&eacute;monde, afin qu&#39;il porte encore plus de fruit.</p>

<p><sup class="versenum">3&nbsp;</sup>D&eacute;j&agrave; vous &ecirc;tes purs, &agrave; cause de la parole que je vous ai annonc&eacute;e.</p>

<p><sup class="versenum">4&nbsp;</sup>Demeurez en moi, et je demeurerai en vous. Comme le sarment ne peut de lui-m&ecirc;me porter du fruit, s&#39;il ne demeure attach&eacute; au cep, ainsi vous ne le pouvez non plus, si vous ne demeurez en moi.</p>

<p><sup class="versenum">5&nbsp;</sup>Je suis le cep, vous &ecirc;tes les sarments. Celui qui demeure en moi et en qui je demeure porte beaucoup de fruit, car sans moi vous ne pouvez rien faire.</p>

<p><sup class="versenum">6&nbsp;</sup>Si quelqu&#39;un ne demeure pas en moi, il est jet&eacute; dehors, comme le sarment, et il s&egrave;che; puis on ramasse les sarments, on les jette au feu, et ils br&ucirc;lent.</p>

<p><sup class="versenum">7&nbsp;</sup>Si vous demeurez en moi, et que mes paroles demeurent en vous, demandez ce que vous voudrez, et cela vous sera accord&eacute;.</p>

<p><sup class="versenum">8&nbsp;</sup>Si vous portez beaucoup de fruit, c&#39;est ainsi que mon P&egrave;re sera glorifi&eacute;, et que vous serez mes disciples.</p>

<p><sup class="versenum">9&nbsp;</sup>Comme le P&egrave;re m&#39;a aim&eacute;, je vous ai aussi aim&eacute;s. Demeurez dans mon amour.</p>

<p><sup class="versenum">10&nbsp;</sup>Si vous gardez mes commandements, vous demeurerez dans mon amour, de m&ecirc;me que j&#39;ai gard&eacute; les commandements de mon P&egrave;re, et que je demeure dans son amour.</p>

<p><sup class="versenum">11&nbsp;</sup>Je vous ai dit ces choses, afin que ma joie soit en vous, et que votre joie soit parfaite.</p>

<p><sup class="versenum">12&nbsp;</sup>C&#39;est ici mon commandement: Aimez-vous les uns les autres, comme je vous ai aim&eacute;s.</p>

<p><sup class="versenum">13&nbsp;</sup>Il n&#39;y a pas de plus grand amour que de donner sa vie pour ses amis.</p>

<p><sup class="versenum">14&nbsp;</sup>Vous &ecirc;tes mes amis, si vous faites ce que je vous commande.</p>

<p><sup class="versenum">15&nbsp;</sup>Je ne vous appelle plus serviteurs, parce que le serviteur ne sait pas ce que fait son ma&icirc;tre; mais je vous ai appel&eacute;s amis, parce que je vous ai fait conna&icirc;tre tout ce que j&#39;ai appris de mon P&egrave;re.</p>

<p><sup class="versenum">16&nbsp;</sup>Ce n&#39;est pas vous qui m&#39;avez choisi; mais moi, je vous ai choisis, et je vous ai &eacute;tablis, afin que vous alliez, et que vous portiez du fruit, et que votre fruit demeure, afin que ce que vous demanderez au P&egrave;re en mon nom, il vous le donne.</p>

<p><sup class="versenum">17&nbsp;</sup>Ce que je vous commande, c&#39;est de vous aimer les uns les autres.</p>

<p><sup class="versenum">18&nbsp;</sup>Si le monde vous hait, sachez qu&#39;il m&#39;a ha&iuml; avant vous.</p>

<p><sup class="versenum">19&nbsp;</sup>Si vous &eacute;tiez du monde, le monde aimerait ce qui est &agrave; lui; mais parce que vous n&#39;&ecirc;tes pas du monde, et que je vous ai choisis du milieu du monde, &agrave; cause de cela le monde vous hait.</p>

<p><sup class="versenum">20&nbsp;</sup>Souvenez-vous de la parole que je vous ai dite: Le serviteur n&#39;est pas plus grand que son ma&icirc;tre. S&#39;ils m&#39;ont pers&eacute;cut&eacute;, ils vous pers&eacute;cuteront aussi; s&#39;ils ont gard&eacute; ma parole, ils garderont aussi la v&ocirc;tre.</p>

<p><sup class="versenum">21&nbsp;</sup>Mais ils vous feront toutes ces choses &agrave; cause de mon nom, parce qu&#39;ils ne connaissent pas celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">22&nbsp;</sup>Si je n&#39;&eacute;tais pas venu et que je ne leur eusses point parl&eacute;, ils n&#39;auraient pas de p&eacute;ch&eacute;; mais maintenant ils n&#39;ont aucune excuse de leur p&eacute;ch&eacute;.</p>

<p><sup class="versenum">23&nbsp;</sup>Celui qui me hait, hait aussi mon P&egrave;re.</p>

<p><sup class="versenum">24&nbsp;</sup>Si je n&#39;avais pas fait parmi eux des oeuvres que nul autre n&#39;a faites, ils n&#39;auraient pas de p&eacute;ch&eacute;; mais maintenant ils les ont vues, et ils ont ha&iuml; et moi et mon P&egrave;re.</p>

<p><sup class="versenum">25&nbsp;</sup>Mais cela est arriv&eacute; afin que s&#39;accompl&icirc;t la parole qui est &eacute;crite dans leur loi: Ils m&#39;ont ha&iuml; sans cause.</p>

<p><sup class="versenum">26&nbsp;</sup>Quand sera venu le consolateur, que je vous enverrai de la part du P&egrave;re, l&#39;Esprit de v&eacute;rit&eacute;, qui vient du P&egrave;re, il rendra t&eacute;moignage de moi;</p>

<p><sup class="versenum">27&nbsp;</sup>et vous aussi, vous rendrez t&eacute;moignage, parce que vous &ecirc;tes avec moi d&egrave;s le commencement.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible --></div>
&nbsp;C&#39;est par la pr&eacute;sence et la puissance de l&#39;Esprit que les hommes et les femmes continuent la mission de J&eacute;sus.

<p>&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Le Saint-Esprit est venu le jour de la Pentecôte: ', '/content/M2/fra/multiply3/multiply303.html')">
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