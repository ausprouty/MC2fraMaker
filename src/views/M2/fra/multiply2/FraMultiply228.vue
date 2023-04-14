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
                        <div class="chapter_number ltr"><h1>28.</h1></div>
                        <div class="chapter_title ltr"><h1>Le plan du Père</h1></div>
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
	<li>Lisez ou observez Luc 6:27-49 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 6:27-49</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">27&nbsp;</sup>Mais je vous dis, &agrave; vous qui m&#39;&eacute;coutez: Aimez vos ennemis, faites du bien &agrave; ceux qui vous ha&iuml;ssent,</p>

<p><sup class="versenum">28&nbsp;</sup>b&eacute;nissez ceux qui vous maudissent, priez pour ceux qui vous maltraitent.</p>

<p><sup class="versenum">29&nbsp;</sup>Si quelqu&#39;un te frappe sur une joue, pr&eacute;sente-lui aussi l&#39;autre. Si quelqu&#39;un prend ton manteau, ne l&#39;emp&ecirc;che pas de prendre encore ta tunique.</p>

<p><sup class="versenum">30&nbsp;</sup>Donne &agrave; quiconque te demande, et ne r&eacute;clame pas ton bien &agrave; celui qui s&#39;en empare.</p>

<p><sup class="versenum">31&nbsp;</sup>Ce que vous voulez que les hommes fassent pour vous, faites-le de m&ecirc;me pour eux.</p>

<p><sup class="versenum">32&nbsp;</sup>Si vous aimez ceux qui vous aiment, quel gr&eacute; vous en saura-t-on? Les p&eacute;cheurs aussi aiment ceux qui les aiment.</p>

<p><sup class="versenum">33&nbsp;</sup>Si vous faites du bien &agrave; ceux qui vous font du bien, quel gr&eacute; vous en saura-t-on? Les p&eacute;cheurs aussi agissent de m&ecirc;me.</p>

<p><sup class="versenum">34&nbsp;</sup>Et si vous pr&ecirc;tez &agrave; ceux de qui vous esp&eacute;rez recevoir, quel gr&eacute; vous en saura-t-on? Les p&eacute;cheurs aussi pr&ecirc;tent aux p&eacute;cheurs, afin de recevoir la pareille.</p>

<p><sup class="versenum">35&nbsp;</sup>Mais aimez vos ennemis, faites du bien, et pr&ecirc;tez sans rien esp&eacute;rer. Et votre r&eacute;compense sera grande, et vous serez fils du Tr&egrave;s Haut, car il est bon pour les ingrats et pour les m&eacute;chants.</p>

<p><sup class="versenum">36&nbsp;</sup>Soyez donc mis&eacute;ricordieux, comme votre P&egrave;re est mis&eacute;ricordieux.</p>

<p><sup class="versenum">37&nbsp;</sup>Ne jugez point, et vous ne serez point jug&eacute;s; ne condamnez point, et vous ne serez point condamn&eacute;s; absolvez, et vous serez absous.</p>

<p><sup class="versenum">38&nbsp;</sup>Donnez, et il vous sera donn&eacute;: on versera dans votre sein une bonne mesure, serr&eacute;e, secou&eacute;e et qui d&eacute;borde; car on vous mesurera avec la mesure dont vous vous serez servis.</p>

<p><sup class="versenum">39&nbsp;</sup>Il leur dit aussi cette parabole: Un aveugle peut-il conduire un aveugle? Ne tomberont-ils pas tous deux dans une fosse?</p>

<p><sup class="versenum">40&nbsp;</sup>Le disciple n&#39;est pas plus que le ma&icirc;tre; mais tout disciple accompli sera comme son ma&icirc;tre.</p>

<p><sup class="versenum">41&nbsp;</sup>Pourquoi vois-tu la paille qui est dans l&#39;oeil de ton fr&egrave;re, et n&#39;aper&ccedil;ois-tu pas la poutre qui est dans ton oeil?</p>

<p><sup class="versenum">42&nbsp;</sup>Ou comment peux-tu dire &agrave; ton fr&egrave;re: Fr&egrave;re, laisse-moi &ocirc;ter la paille qui est dans ton oeil, toi qui ne vois pas la poutre qui est dans le tien? Hypocrite, &ocirc;te premi&egrave;rement la poutre de ton oeil, et alors tu verras comment &ocirc;ter la paille qui est dans l&#39;oeil de ton fr&egrave;re.</p>

<p><sup class="versenum">43&nbsp;</sup>Ce n&#39;est pas un bon arbre qui porte du mauvais fruit, ni un mauvais arbre qui porte du bon fruit.</p>

<p><sup class="versenum">44&nbsp;</sup>Car chaque arbre se conna&icirc;t &agrave; son fruit. On ne cueille pas des figues sur des &eacute;pines, et l&#39;on ne vendange pas des raisins sur des ronces.</p>

<p><sup class="versenum">45&nbsp;</sup>L&#39;homme bon tire de bonnes choses du bon tr&eacute;sor de son coeur, et le m&eacute;chant tire de mauvaises choses de son mauvais tr&eacute;sor; car c&#39;est de l&#39;abondance du coeur que la bouche parle.</p>

<p><sup class="versenum">46&nbsp;</sup>Pourquoi m&#39;appelez-vous Seigneur, Seigneur! et ne faites-vous pas ce que je dis?</p>

<p><sup class="versenum">47&nbsp;</sup>Je vous montrerai &agrave; qui est semblable tout homme qui vient &agrave; moi, entend mes paroles, et les met en pratique.</p>

<p><sup class="versenum">48&nbsp;</sup>Il est semblable &agrave; un homme qui, b&acirc;tissant une maison, a creus&eacute;, creus&eacute; profond&eacute;ment, et a pos&eacute; le fondement sur le roc. Une inondation est venue, et le torrent s&#39;est jet&eacute; contre cette maison, sans pouvoir l&#39;&eacute;branler, parce qu&#39;elle &eacute;tait bien b&acirc;tie.</p>

<p><sup class="versenum">49&nbsp;</sup>Mais celui qui entend, et ne met pas en pratique, est semblable &agrave; un homme qui a b&acirc;ti une maison sur la terre, sans fondement. Le torrent s&#39;est jet&eacute; contre elle: aussit&ocirc;t elle est tomb&eacute;e, et la ruine de cette maison a &eacute;t&eacute; grande.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/228.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 6:27-49&nbsp; </button>
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

<p>J&eacute;sus explique la vie future dans le Royaume aux disciples. Une partie du plan pour l&#39;expansion du Royaume est d&rsquo;aimer vos ennemis. C&#39;est un amour qui n&#39;attend rien en retour. C&#39;est un amour radical, divin, qui va changer le monde. Une partie de l&#39;amour des autres comprend, arr&ecirc;ter de juger les autres et arr&ecirc;ter de condamner les autres pour leurs actions. Au lieu de cela, &eacute;tendez le pardon au nom de J&eacute;sus, non pas parce qu&#39;ils le m&eacute;ritent mais parce qu&#39;Il nous le demande. Nous devrons prendre le temps d&#39;examiner nos propres vies. Il instruit les dirigeants avec &laquo;l&rsquo;aveugle ne peut pas conduire l&rsquo;aveugle&raquo;, ils ont besoin de s&rsquo;approprier ce style de vie. Il leur rappelle qu&#39;ils ont besoin de regarder sa vie et son minist&egrave;re de pr&egrave;s. &laquo; Ne m&#39;appelez pas Seigneur si vous ne faites pas ce que je dis. &raquo;</p>

<p>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Matthieu 5:17-8:1</span></p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<div>
<div>
<div>
<div>
<div>
<div>
<p><sup class="versenum">5:17&nbsp;</sup>Ne croyez pas que je sois venu pour abolir la loi ou les proph&egrave;tes; je suis venu non pour abolir, mais pour accomplir.</p>

<p><sup class="versenum">18&nbsp;</sup>Car, je vous le dis en v&eacute;rit&eacute;, tant que le ciel et la terre ne passeront point, il ne dispara&icirc;tra pas de la loi un seul iota ou un seul trait de lettre, jusqu&#39;&agrave; ce que tout soit arriv&eacute;.</p>

<p><sup class="versenum">19&nbsp;</sup>Celui donc qui supprimera l&#39;un de ces plus petits commandements, et qui enseignera aux hommes &agrave; faire de m&ecirc;me, sera appel&eacute; le plus petit dans le royaume des cieux; mais celui qui les observera, et qui enseignera &agrave; les observer, celui-l&agrave; sera appel&eacute; grand dans le royaume des cieux.</p>

<p><sup class="versenum">20&nbsp;</sup>Car, je vous le dis, si votre justice ne surpasse celle des scribes et des pharisiens, vous n&#39;entrerez point dans le royaume des cieux.</p>

<p><sup class="versenum">21&nbsp;</sup>Vous avez entendu qu&#39;il a &eacute;t&eacute; dit aux anciens: Tu ne tueras point; celui qui tuera m&eacute;rite d&#39;&ecirc;tre puni par les juges.</p>

<p><sup class="versenum">22&nbsp;</sup>Mais moi, je vous dis que quiconque se met en col&egrave;re contre son fr&egrave;re m&eacute;rite d&#39;&ecirc;tre puni par les juges; que celui qui dira &agrave; son fr&egrave;re: Raca! m&eacute;rite d&#39;&ecirc;tre puni par le sanh&eacute;drin; et que celui qui lui dira: Insens&eacute;! m&eacute;rite d&#39;&ecirc;tre puni par le feu de la g&eacute;henne.</p>

<p><sup class="versenum">23&nbsp;</sup>Si donc tu pr&eacute;sentes ton offrande &agrave; l&#39;autel, et que l&agrave; tu te souviennes que ton fr&egrave;re a quelque chose contre toi,</p>

<p><sup class="versenum">24&nbsp;</sup>laisse l&agrave; ton offrande devant l&#39;autel, et va d&#39;abord te r&eacute;concilier avec ton fr&egrave;re; puis, viens pr&eacute;senter ton offrande.</p>

<p><sup class="versenum">25&nbsp;</sup>Accorde-toi promptement avec ton adversaire, pendant que tu es en chemin avec lui, de peur qu&#39;il ne te livre au juge, que le juge ne te livre &agrave; l&#39;officier de justice, et que tu ne sois mis en prison.</p>

<p><sup class="versenum">26&nbsp;</sup>Je te le dis en v&eacute;rit&eacute;, tu ne sortiras pas de l&agrave; que tu n&#39;aies pay&eacute; le dernier quadrant.</p>

<p><sup class="versenum">27&nbsp;</sup>Vous avez appris qu&#39;il a &eacute;t&eacute; dit: Tu ne commettras point d&#39;adult&egrave;re.</p>

<p><sup class="versenum">28&nbsp;</sup>Mais moi, je vous dis que quiconque regarde une femme pour la convoiter a d&eacute;j&agrave; commis un adult&egrave;re avec elle dans son coeur.</p>

<p><sup class="versenum">29&nbsp;</sup>Si ton oeil droit est pour toi une occasion de chute, arrache-le et jette-le loin de toi; car il est avantageux pour toi qu&#39;un seul de tes membres p&eacute;risse, et que ton corps entier ne soit pas jet&eacute; dans la g&eacute;henne.</p>

<p><sup class="versenum">30&nbsp;</sup>Et si ta main droite est pour toi une occasion de chute, coupe-la et jette-la loin de toi; car il est avantageux pour toi qu&#39;un seul de tes membres p&eacute;risse, et que ton corps entier n&#39;aille pas dans la g&eacute;henne.</p>

<p><sup class="versenum">31&nbsp;</sup>Il a &eacute;t&eacute; dit: Que celui qui r&eacute;pudie sa femme lui donne une lettre de divorce.</p>

<p><sup class="versenum">32&nbsp;</sup>Mais moi, je vous dis que celui qui r&eacute;pudie sa femme, sauf pour cause d&#39;infid&eacute;lit&eacute;, l&#39;expose &agrave; devenir adult&egrave;re, et que celui qui &eacute;pouse une femme r&eacute;pudi&eacute;e commet un adult&egrave;re.</p>

<p><sup class="versenum">33&nbsp;</sup>Vous avez encore appris qu&#39;il a &eacute;t&eacute; dit aux anciens: Tu ne te parjureras point, mais tu t&#39;acquitteras envers le Seigneur de ce que tu as d&eacute;clar&eacute; par serment.</p>

<p><sup class="versenum">34&nbsp;</sup>Mais moi, je vous dis de ne jurer aucunement, ni par le ciel, parce que c&#39;est le tr&ocirc;ne de Dieu;</p>

<p><sup class="versenum">35&nbsp;</sup>ni par la terre, parce que c&#39;est son marchepied; ni par J&eacute;rusalem, parce que c&#39;est la ville du grand roi.</p>

<p><sup class="versenum">36&nbsp;</sup>Ne jure pas non plus par ta t&ecirc;te, car tu ne peux rendre blanc ou noir un seul cheveu.</p>

<p><sup class="versenum">37&nbsp;</sup>Que votre parole soit oui, oui, non, non; ce qu&#39;on y ajoute vient du malin.</p>

<p><sup class="versenum">38&nbsp;</sup>Vous avez appris qu&#39;il a &eacute;t&eacute; dit: oeil pour oeil, et dent pour dent.</p>

<p><sup class="versenum">39&nbsp;</sup>Mais moi, je vous dis de ne pas r&eacute;sister au m&eacute;chant. Si quelqu&#39;un te frappe sur la joue droite, pr&eacute;sente-lui aussi l&#39;autre.</p>

<p><sup class="versenum">40&nbsp;</sup>Si quelqu&#39;un veut plaider contre toi, et prendre ta tunique, laisse-lui encore ton manteau.</p>

<p><sup class="versenum">41&nbsp;</sup>Si quelqu&#39;un te force &agrave; faire un mille, fais-en deux avec lui.</p>

<p><sup class="versenum">42&nbsp;</sup>Donne &agrave; celui qui te demande, et ne te d&eacute;tourne pas de celui qui veut emprunter de toi.</p>

<p><sup class="versenum">43&nbsp;</sup>Vous avez appris qu&#39;il a &eacute;t&eacute; dit: Tu aimeras ton prochain, et tu ha&iuml;ras ton ennemi.</p>

<p><sup class="versenum">44&nbsp;</sup>Mais moi, je vous dis: Aimez vos ennemis, b&eacute;nissez ceux qui vous maudissent, faites du bien &agrave; ceux qui vous ha&iuml;ssent, et priez pour ceux qui vous maltraitent et qui vous pers&eacute;cutent,</p>

<p><sup class="versenum">45&nbsp;</sup>afin que vous soyez fils de votre P&egrave;re qui est dans les cieux; car il fait lever son soleil sur les m&eacute;chants et sur les bons, et il fait pleuvoir sur les justes et sur les injustes.</p>

<p><sup class="versenum">46&nbsp;</sup>Si vous aimez ceux qui vous aiment, quelle r&eacute;compense m&eacute;ritez-vous? Les publicains aussi n&#39;agissent-ils pas de m&ecirc;me?</p>

<p><sup class="versenum">47&nbsp;</sup>Et si vous saluez seulement vos fr&egrave;res, que faites-vous d&#39;extraordinaire? Les pa&iuml;ens aussi n&#39;agissent-ils pas de m&ecirc;me?</p>

<p><sup class="versenum">48&nbsp;</sup>Soyez donc parfaits, comme votre P&egrave;re c&eacute;leste est parfait.</p>

<p><sup class="versenum">6:5:1 </sup>Gardez-vous de pratiquer votre justice devant les hommes, pour en &ecirc;tre vus; autrement, vous n&#39;aurez point de r&eacute;compense aupr&egrave;s de votre P&egrave;re qui est dans les cieux.</p>

<p><sup class="versenum">2&nbsp;</sup>Lors donc que tu fais l&#39;aum&ocirc;ne, ne sonne pas de la trompette devant toi, comme font les hypocrites dans les synagogues et dans les rues, afin d&#39;&ecirc;tre glorifi&eacute;s par les hommes. Je vous le dis en v&eacute;rit&eacute;, ils re&ccedil;oivent leur r&eacute;compense.</p>

<p><sup class="versenum">3&nbsp;</sup>Mais quand tu fais l&#39;aum&ocirc;ne, que ta main gauche ne sache pas ce que fait ta droite,</p>

<p><sup class="versenum">4&nbsp;</sup>afin que ton aum&ocirc;ne se fasse en secret; et ton P&egrave;re, qui voit dans le secret, te le rendra.</p>

<p><sup class="versenum">5&nbsp;</sup>Lorsque vous priez, ne soyez pas comme les hypocrites, qui aiment &agrave; prier debout dans les synagogues et aux coins des rues, pour &ecirc;tre vus des hommes. Je vous le dis en v&eacute;rit&eacute;, ils re&ccedil;oivent leur r&eacute;compense.</p>

<p><sup class="versenum">6&nbsp;</sup>Mais quand tu pries, entre dans ta chambre, ferme ta porte, et prie ton P&egrave;re qui est l&agrave; dans le lieu secret; et ton P&egrave;re, qui voit dans le secret, te le rendra.</p>

<p><sup class="versenum">7&nbsp;</sup>En priant, ne multipliez pas de vaines paroles, comme les pa&iuml;ens, qui s&#39;imaginent qu&#39;&agrave; force de paroles ils seront exauc&eacute;s.</p>

<p><sup class="versenum">8&nbsp;</sup>Ne leur ressemblez pas; car votre P&egrave;re sait de quoi vous avez besoin, avant que vous le lui demandiez.</p>

<p><sup class="versenum">9&nbsp;</sup>Voici donc comment vous devez prier: Notre P&egrave;re qui es aux cieux! Que ton nom soit sanctifi&eacute;;</p>

<p><sup class="versenum">10&nbsp;</sup>que ton r&egrave;gne vienne; que ta volont&eacute; soit faite sur la terre comme au ciel.</p>

<p><sup class="versenum">11&nbsp;</sup>Donne-nous aujourd&#39;hui notre pain quotidien;</p>

<p><sup class="versenum">12&nbsp;</sup>pardonne-nous nos offenses, comme nous aussi nous pardonnons &agrave; ceux qui nous ont offens&eacute;s;</p>

<p><sup class="versenum">13&nbsp;</sup>ne nous induis pas en tentation, mais d&eacute;livre-nous du malin. Car c&#39;est &agrave; toi qu&#39;appartiennent, dans tous les si&egrave;cles, le r&egrave;gne, la puissance et la gloire. Amen!</p>

<p><sup class="versenum">14&nbsp;</sup>Si vous pardonnez aux hommes leurs offenses, votre P&egrave;re c&eacute;leste vous pardonnera aussi;</p>

<p><sup class="versenum">15&nbsp;</sup>mais si vous ne pardonnez pas aux hommes, votre P&egrave;re ne vous pardonnera pas non plus vos offenses.</p>

<p><sup class="versenum">16&nbsp;</sup>Lorsque vous je&ucirc;nez, ne prenez pas un air triste, comme les hypocrites, qui se rendent le visage tout d&eacute;fait, pour montrer aux hommes qu&#39;ils je&ucirc;nent. Je vous le dis en v&eacute;rit&eacute;, ils re&ccedil;oivent leur r&eacute;compense.</p>

<p><sup class="versenum">17&nbsp;</sup>Mais quand tu je&ucirc;nes, parfume ta t&ecirc;te et lave ton visage,</p>

<p><sup class="versenum">18&nbsp;</sup>afin de ne pas montrer aux hommes que tu je&ucirc;nes, mais &agrave; ton P&egrave;re qui est l&agrave; dans le lieu secret; et ton P&egrave;re, qui voit dans le secret, te le rendra.</p>

<p><sup class="versenum">19&nbsp;</sup>Ne vous amassez pas des tr&eacute;sors sur la terre, o&ugrave; la teigne et la rouille d&eacute;truisent, et o&ugrave; les voleurs percent et d&eacute;robent;</p>

<p><sup class="versenum">20&nbsp;</sup>mais amassez-vous des tr&eacute;sors dans le ciel, o&ugrave; la teigne et la rouille ne d&eacute;truisent point, et o&ugrave; les voleurs ne percent ni ne d&eacute;robent.</p>

<p><sup class="versenum">21&nbsp;</sup>Car l&agrave; o&ugrave; est ton tr&eacute;sor, l&agrave; aussi sera ton coeur.</p>

<p><sup class="versenum">22&nbsp;</sup>L&#39;oeil est la lampe du corps. Si ton oeil est en bon &eacute;tat, tout ton corps sera &eacute;clair&eacute;;</p>

<p><sup class="versenum">23&nbsp;</sup>mais si ton oeil est en mauvais &eacute;tat, tout ton corps sera dans les t&eacute;n&egrave;bres. Si donc la lumi&egrave;re qui est en toi est t&eacute;n&egrave;bres, combien seront grandes ces t&eacute;n&egrave;bres!</p>

<p><sup class="versenum">24&nbsp;</sup>Nul ne peut servir deux ma&icirc;tres. Car, ou il ha&iuml;ra l&#39;un, et aimera l&#39;autre; ou il s&#39;attachera &agrave; l&#39;un, et m&eacute;prisera l&#39;autre. Vous ne pouvez servir Dieu et Mamon.</p>

<p><sup class="versenum">25&nbsp;</sup>C&#39;est pourquoi je vous dis: Ne vous inqui&eacute;tez pas pour votre vie de ce que vous mangerez, ni pour votre corps, de quoi vous serez v&ecirc;tus. La vie n&#39;est-elle pas plus que la nourriture, et le corps plus que le v&ecirc;tement?</p>

<p><sup class="versenum">26&nbsp;</sup>Regardez les oiseaux du ciel: ils ne s&egrave;ment ni ne moissonnent, et ils n&#39;amassent rien dans des greniers; et votre P&egrave;re c&eacute;leste les nourrit. Ne valez-vous pas beaucoup plus qu&#39;eux?</p>

<p><sup class="versenum">27&nbsp;</sup>Qui de vous, par ses inqui&eacute;tudes, peut ajouter une coud&eacute;e &agrave; la dur&eacute;e de sa vie?</p>

<p><sup class="versenum">28&nbsp;</sup>Et pourquoi vous inqui&eacute;ter au sujet du v&ecirc;tement? Consid&eacute;rez comment croissent les lis des champs: ils ne travaillent ni ne filent;</p>

<p><sup class="versenum">29&nbsp;</sup>cependant je vous dis que Salomon m&ecirc;me, dans toute sa gloire, n&#39;a pas &eacute;t&eacute; v&ecirc;tu comme l&#39;un d&#39;eux.</p>

<p><sup class="versenum">30&nbsp;</sup>Si Dieu rev&ecirc;t ainsi l&#39;herbe des champs, qui existe aujourd&#39;hui et qui demain sera jet&eacute;e au four, ne vous v&ecirc;tira-t-il pas &agrave; plus forte raison, gens de peu de foi?</p>

<p><sup class="versenum">31&nbsp;</sup>Ne vous inqui&eacute;tez donc point, et ne dites pas: Que mangerons-nous? que boirons-nous? de quoi serons-nous v&ecirc;tus?</p>

<p><sup class="versenum">32&nbsp;</sup>Car toutes ces choses, ce sont les pa&iuml;ens qui les recherchent. Votre P&egrave;re c&eacute;leste sait que vous en avez besoin.</p>

<p><sup class="versenum">33&nbsp;</sup>Cherchez premi&egrave;rement le royaume et la justice de Dieu; et toutes ces choses vous seront donn&eacute;es par-dessus.</p>

<p><sup class="versenum">34&nbsp;</sup>Ne vous inqui&eacute;tez donc pas du lendemain; car le lendemain aura soin de lui-m&ecirc;me. A chaque jour suffit sa peine.</p>

<p><sup class="versenum">7:1 </sup>Ne jugez point, afin que vous ne soyez point jug&eacute;s.</p>

<p><sup class="versenum">2&nbsp;</sup>Car on vous jugera du jugement dont vous jugez, et l&#39;on vous mesurera avec la mesure dont vous mesurez.</p>

<p><sup class="versenum">3&nbsp;</sup>Pourquoi vois-tu la paille qui est dans l&#39;oeil de ton fr&egrave;re, et n&#39;aper&ccedil;ois-tu pas la poutre qui est dans ton oeil?</p>

<p><sup class="versenum">4&nbsp;</sup>Ou comment peux-tu dire &agrave; ton fr&egrave;re: Laisse-moi &ocirc;ter une paille de ton oeil, toi qui as une poutre dans le tien?</p>

<p><sup class="versenum">5&nbsp;</sup>Hypocrite, &ocirc;te premi&egrave;rement la poutre de ton oeil, et alors tu verras comment &ocirc;ter la paille de l&#39;oeil de ton fr&egrave;re.</p>

<p><sup class="versenum">6&nbsp;</sup>Ne donnez pas les choses saintes aux chiens, et ne jetez pas vos perles devant les pourceaux, de peur qu&#39;ils ne les foulent aux pieds, ne se retournent et ne vous d&eacute;chirent.</p>

<p><sup class="versenum">7&nbsp;</sup>Demandez, et l&#39;on vous donnera; cherchez, et vous trouverez; frappez, et l&#39;on vous ouvrira.</p>

<p><sup class="versenum">8&nbsp;</sup>Car quiconque demande re&ccedil;oit, celui qui cherche trouve, et l&#39;on ouvre &agrave; celui qui frappe.</p>

<p><sup class="versenum">9&nbsp;</sup>Lequel de vous donnera une pierre &agrave; son fils, s&#39;il lui demande du pain?</p>

<p><sup class="versenum">10&nbsp;</sup>Ou, s&#39;il demande un poisson, lui donnera-t-il un serpent?</p>

<p><sup class="versenum">11&nbsp;</sup>Si donc, m&eacute;chants comme vous l&#39;&ecirc;tes, vous savez donner de bonnes choses &agrave; vos enfants, &agrave; combien plus forte raison votre P&egrave;re qui est dans les cieux donnera-t-il de bonnes choses &agrave; ceux qui les lui demandent.</p>

<p><sup class="versenum">12&nbsp;</sup>Tout ce que vous voulez que les hommes fassent pour vous, faites-le de m&ecirc;me pour eux, car c&#39;est la loi et les proph&egrave;tes.</p>

<p><sup class="versenum">13&nbsp;</sup>Entrez par la porte &eacute;troite. Car large est la porte, spacieux est le chemin qui m&egrave;nent &agrave; la perdition, et il y en a beaucoup qui entrent par l&agrave;.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais &eacute;troite est la porte, resserr&eacute; le chemin qui m&egrave;nent &agrave; la vie, et il y en a peu qui les trouvent.</p>

<p><sup class="versenum">15&nbsp;</sup>Gardez-vous des faux proph&egrave;tes. Ils viennent &agrave; vous en v&ecirc;tement de brebis, mais au dedans ce sont des loups ravisseurs.</p>

<p><sup class="versenum">16&nbsp;</sup>Vous les reconna&icirc;trez &agrave; leurs fruits. Cueille-t-on des raisins sur des &eacute;pines, ou des figues sur des chardons?</p>

<p><sup class="versenum">17&nbsp;</sup>Tout bon arbre porte de bons fruits, mais le mauvais arbre porte de mauvais fruits.</p>

<p><sup class="versenum">18&nbsp;</sup>Un bon arbre ne peut porter de mauvais fruits, ni un mauvais arbre porter de bons fruits.</p>

<p><sup class="versenum">19&nbsp;</sup>Tout arbre qui ne porte pas de bons fruits est coup&eacute; et jet&eacute; au feu.</p>

<p><sup class="versenum">20&nbsp;</sup>C&#39;est donc &agrave; leurs fruits que vous les reconna&icirc;trez.</p>

<p><sup class="versenum">21&nbsp;</sup>Ceux qui me disent: Seigneur, Seigneur! n&#39;entreront pas tous dans le royaume des cieux, mais celui-l&agrave; seul qui fait la volont&eacute; de mon P&egrave;re qui est dans les cieux.</p>

<p><sup class="versenum">22&nbsp;</sup>Plusieurs me diront en ce jour-l&agrave;: Seigneur, Seigneur, n&#39;avons-nous pas proph&eacute;tis&eacute; par ton nom? n&#39;avons-nous pas chass&eacute; des d&eacute;mons par ton nom? et n&#39;avons-nous pas fait beaucoup de miracles par ton nom?</p>

<p><sup class="versenum">23&nbsp;</sup>Alors je leur dirai ouvertement: Je ne vous ai jamais connus, retirez-vous de moi, vous qui commettez l&#39;iniquit&eacute;.</p>

<p><sup class="versenum">24&nbsp;</sup>C&#39;est pourquoi, quiconque entend ces paroles que je dis et les met en pratique, sera semblable &agrave; un homme prudent qui a b&acirc;ti sa maison sur le roc.</p>

<p><sup class="versenum">25&nbsp;</sup>La pluie est tomb&eacute;e, les torrents sont venus, les vents ont souffl&eacute; et se sont jet&eacute;s contre cette maison: elle n&#39;est point tomb&eacute;e, parce qu&#39;elle &eacute;tait fond&eacute;e sur le roc.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais quiconque entend ces paroles que je dis, et ne les met pas en pratique, sera semblable &agrave; un homme insens&eacute; qui a b&acirc;ti sa maison sur le sable.</p>

<p><sup class="versenum">27&nbsp;</sup>La pluie est tomb&eacute;e, les torrents sont venus, les vents ont souffl&eacute; et ont battu cette maison: elle est tomb&eacute;e, et sa ruine a &eacute;t&eacute; grande.</p>

<p><sup class="versenum">28&nbsp;</sup>Apr&egrave;s que J&eacute;sus eut achev&eacute; ces discours, la foule fut frapp&eacute;e de sa doctrine;</p>

<p><sup class="versenum">29&nbsp;</sup>car il enseignait comme ayant autorit&eacute;, et non pas comme leurs scribes.</p>

<p><sup class="versenum">8:1 </sup>Lorsque J&eacute;sus fut descendu de la montagne, une grande foule le suivit.</p>
</div>
</div>
</div>
</div>
</div>
</div>
<!-- end bible --></div>
&nbsp;

<p>&nbsp;</p>

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

			<td class="social" @click="share('lesson', 'Le plan du Père: ', '/content/M2/fra/multiply2/multiply228.html')">
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