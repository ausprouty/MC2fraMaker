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
                        <div class="chapter_number ltr"><h1>49.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership de la Croix</h1></div>
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
	<li>Lisez ou observez Jean 19:13-30; Matthieu 27:45-46 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 19:13-30</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">13&nbsp;</sup>Pilate, ayant entendu ces paroles, amena J&eacute;sus dehors; et il s&#39;assit sur le tribunal, au lieu appel&eacute; le Pav&eacute;, et en h&eacute;breu Gabbatha.</p>

<p><sup class="versenum">14&nbsp;</sup>C&#39;&eacute;tait la pr&eacute;paration de la P&acirc;que, et environ la sixi&egrave;me heure. Pilate dit aux Juifs: Voici votre roi.</p>

<p><sup class="versenum">15&nbsp;</sup>Mais ils s&#39;&eacute;cri&egrave;rent: Ote, &ocirc;te, crucifie-le! Pilate leur dit: Crucifierai-je votre roi? Les principaux sacrificateurs r&eacute;pondirent: Nous n&#39;avons de roi que C&eacute;sar.</p>

<p><sup class="versenum">16&nbsp;</sup>Alors il le leur livra pour &ecirc;tre crucifi&eacute;. Ils prirent donc J&eacute;sus, et l&#39;emmen&egrave;rent.</p>

<p><sup class="versenum">17&nbsp;</sup>J&eacute;sus, portant sa croix, arriva au lieu du cr&acirc;ne, qui se nomme en h&eacute;breu Golgotha.</p>

<p><sup class="versenum">18&nbsp;</sup>C&#39;est l&agrave; qu&#39;il fut crucifi&eacute;, et deux autres avec lui, un de chaque c&ocirc;t&eacute;, et J&eacute;sus au milieu.</p>

<p><sup class="versenum">19&nbsp;</sup>Pilate fit une inscription, qu&#39;il pla&ccedil;a sur la croix, et qui &eacute;tait ainsi con&ccedil;ue: J&eacute;sus de Nazareth, roi des Juifs.</p>

<p><sup class="versenum">20&nbsp;</sup>Beaucoup de Juifs lurent cette inscription, parce que le lieu o&ugrave; J&eacute;sus fut crucifi&eacute; &eacute;tait pr&egrave;s de la ville: elle &eacute;tait en h&eacute;breu, en grec et en latin.</p>

<p><sup class="versenum">21&nbsp;</sup>Les principaux sacrificateurs des Juifs dirent &agrave; Pilate: N&#39;&eacute;cris pas: Roi des Juifs. Mais &eacute;cris qu&#39;il a dit: Je suis roi des Juifs.</p>

<p><sup class="versenum">22&nbsp;</sup>Pilate r&eacute;pondit: Ce que j&#39;ai &eacute;crit, je l&#39;ai &eacute;crit.</p>

<p><sup class="versenum">23&nbsp;</sup>Les soldats, apr&egrave;s avoir crucifi&eacute; J&eacute;sus, prirent ses v&ecirc;tements, et ils en firent quatre parts, une part pour chaque soldat. Ils prirent aussi sa tunique, qui &eacute;tait sans couture, d&#39;un seul tissu depuis le haut jusqu&#39;en bas. Et ils dirent entre eux:</p>

<p><sup class="versenum">24&nbsp;</sup>Ne la d&eacute;chirons pas, mais tirons au sort &agrave; qui elle sera. Cela arriva afin que s&#39;accompl&icirc;t cette parole de l&#39;&Eacute;criture: Ils se sont partag&eacute; mes v&ecirc;tements, Et ils ont tir&eacute; au sort ma tunique. Voil&agrave; ce que firent les soldats.</p>

<p><sup class="versenum">25&nbsp;</sup>Pr&egrave;s de la croix de J&eacute;sus se tenaient sa m&egrave;re et la soeur de sa m&egrave;re, Marie, femme de Clopas, et Marie de Magdala.</p>

<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus, voyant sa m&egrave;re, et aupr&egrave;s d&#39;elle le disciple qu&#39;il aimait, dit &agrave; sa m&egrave;re: Femme, voil&agrave; ton fils.</p>

<p><sup class="versenum">27&nbsp;</sup>Puis il dit au disciple: Voil&agrave; ta m&egrave;re. Et, d&egrave;s ce moment, le disciple la prit chez lui.</p>

<p><sup class="versenum">28&nbsp;</sup>Apr&egrave;s cela, J&eacute;sus, qui savait que tout &eacute;tait d&eacute;j&agrave; consomm&eacute;, dit, afin que l&#39;&Eacute;criture f&ucirc;t accomplie: J&#39;ai soif.</p>

<p><sup class="versenum">29&nbsp;</sup>Il y avait l&agrave; un vase plein de vinaigre. Les soldats en remplirent une &eacute;ponge, et, l&#39;ayant fix&eacute;e &agrave; une branche d&#39;hysope, ils l&#39;approch&egrave;rent de sa bouche.</p>

<p><sup class="versenum">30&nbsp;</sup>Quand J&eacute;sus eut pris le vinaigre, il dit: Tout est accompli. Et, baissant la t&ecirc;te, il rendit l&#39;esprit.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/249.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 19:13-30&nbsp; </button>
    <div class="collapsed"></div>

<button id="Button1" type="button" class="collapsible bible">Lire Matthieu 27:45-46</button><div class="collapsed" id ="Text1">
<!-- begin bible -->

<p><sup class="versenum">45&nbsp;</sup>Depuis la sixi&egrave;me heure jusqu&#39;&agrave; la neuvi&egrave;me, il y eut des t&eacute;n&egrave;bres sur toute la terre.</p>

<p><sup class="versenum">46&nbsp;</sup>Et vers la neuvi&egrave;me heure, J&eacute;sus s&#39;&eacute;cria d&#39;une voix forte: &Eacute;li, &Eacute;li, lama sabachthani? c&#39;est-&agrave;-dire: Mon Dieu, mon Dieu, pourquoi m&#39;as-tu abandonn&eacute;?</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/249-1.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 27:45-46&nbsp; </button>
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

<p>J&eacute;sus a &eacute;t&eacute; trahi, ils ont menti sur Lui, a &eacute;t&eacute; trait&eacute; injustement, battu, fouett&eacute; et finalement clou&eacute; &agrave; une croix pour mourir entre deux criminels. Dans son humanit&eacute;, J&eacute;sus a beaucoup souffert dans ces derni&egrave;res heures de la vie. Dieu a plac&eacute; le p&eacute;ch&eacute; du monde sur J&eacute;sus comme un substitut innocent pour nous. J&eacute;sus a souffert la s&eacute;paration du P&egrave;re pour la premi&egrave;re fois. Il a &eacute;t&eacute; abandonn&eacute; par le P&egrave;re, qui a tourn&eacute; le dos &agrave; J&eacute;sus parce qu&#39;il portait tout le poids du p&eacute;ch&eacute; du monde. L&#39;Agneau de la P&acirc;que de Dieu a fait couler son sang et d&eacute;chir&eacute; le voile du temple. J&eacute;sus &eacute;tait le dernier sacrifice. Maintenant nous avons acc&egrave;s au Dieu vivant. Ceux qui croient ont &eacute;t&eacute; adopt&eacute;s dans cette nouvelle famille. Il a trac&eacute; un chemin vers le P&egrave;re. Il a donn&eacute; sa vie pour payer notre dette. Sur la croix, un grand &eacute;change s&#39;est produit: &laquo; Celui qui n&rsquo;a point connu le p&eacute;ch&eacute;, Il l&rsquo;a fait devenir p&eacute;ch&eacute; pour nous, afin que nous devenions en Lui justice de Dieu. &raquo; (<span class="popup-link" @click = "popUp('pop1')"> 2 Corinthiens 5:21</span>)</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">21&nbsp;</sup>Celui qui n&#39;a point connu le p&eacute;ch&eacute;, il l&#39;a fait devenir p&eacute;ch&eacute; pour nous, afin que nous devenions en lui justice de Dieu.</p>
<!-- end bible --></div>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop2')"> Luc 23:26-49</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">26&nbsp;</sup>Comme ils l&#39;emmenaient, ils prirent un certain Simon de Cyr&egrave;ne, qui revenait des champs, et ils le charg&egrave;rent de la croix, pour qu&#39;il la porte derri&egrave;re J&eacute;sus.</p>

	<p><sup class="versenum">27&nbsp;</sup>Il &eacute;tait suivi d&#39;une grande multitude des gens du peuple, et de femmes qui se frappaient la poitrine et se lamentaient sur lui.</p>

	<p><sup class="versenum">28&nbsp;</sup>J&eacute;sus se tourna vers elles, et dit: Filles de J&eacute;rusalem, ne pleurez pas sur moi; mais pleurez sur vous et sur vos enfants.</p>

	<p><sup class="versenum">29&nbsp;</sup>Car voici, des jours viendront o&ugrave; l&#39;on dira: Heureuses les st&eacute;riles, heureuses les entrailles qui n&#39;ont point enfant&eacute;, et les mamelles qui n&#39;ont point allait&eacute;!</p>

	<p><sup class="versenum">30&nbsp;</sup>Alors ils se mettront &agrave; dire aux montagnes: Tombez sur nous! Et aux collines: Couvrez-nous!</p>

	<p><sup class="versenum">31&nbsp;</sup>Car, si l&#39;on fait ces choses au bois vert, qu&#39;arrivera-t-il au bois sec?</p>

	<p><sup class="versenum">32&nbsp;</sup>On conduisait en m&ecirc;me temps deux malfaiteurs, qui devaient &ecirc;tre mis &agrave; mort avec J&eacute;sus.</p>

	<p><sup class="versenum">33&nbsp;</sup>Lorsqu&#39;ils furent arriv&eacute;s au lieu appel&eacute; Cr&acirc;ne, ils le crucifi&egrave;rent l&agrave;, ainsi que les deux malfaiteurs, l&#39;un &agrave; droite, l&#39;autre &agrave; gauche.</p>

	<p><sup class="versenum">34&nbsp;</sup>J&eacute;sus dit: P&egrave;re, pardonne-leur, car ils ne savent ce qu&#39;ils font. Ils se partag&egrave;rent ses v&ecirc;tements, en tirant au sort.</p>

	<p><sup class="versenum">35&nbsp;</sup>Le peuple se tenait l&agrave;, et regardait. Les magistrats se moquaient de J&eacute;sus, disant: Il a sauv&eacute; les autres; qu&#39;il se sauve lui-m&ecirc;me, s&#39;il est le Christ, l&#39;&eacute;lu de Dieu!</p>

	<p><sup class="versenum">36&nbsp;</sup>Les soldats aussi se moquaient de lui; s&#39;approchant et lui pr&eacute;sentant du vinaigre,</p>

	<p><sup class="versenum">37&nbsp;</sup>ils disaient: Si tu es le roi des Juifs, sauve-toi toi-m&ecirc;me!</p>

	<p><sup class="versenum">38&nbsp;</sup>Il y avait au-dessus de lui cette inscription: Celui-ci est le roi des Juifs.</p>

	<p><sup class="versenum">39&nbsp;</sup>L&#39;un des malfaiteurs crucifi&eacute;s l&#39;injuriait, disant: N&#39;es-tu pas le Christ? Sauve-toi toi-m&ecirc;me, et sauve-nous!</p>

	<p><sup class="versenum">40&nbsp;</sup>Mais l&#39;autre le reprenait, et disait: Ne crains-tu pas Dieu, toi qui subis la m&ecirc;me condamnation?</p>

	<p><sup class="versenum">41&nbsp;</sup>Pour nous, c&#39;est justice, car nous recevons ce qu&#39;ont m&eacute;rit&eacute; nos crimes; mais celui-ci n&#39;a rien fait de mal.</p>

	<p><sup class="versenum">42&nbsp;</sup>Et il dit &agrave; J&eacute;sus: Souviens-toi de moi, quand tu viendras dans ton r&egrave;gne.</p>

	<p><sup class="versenum">43&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Je te le dis en v&eacute;rit&eacute;, aujourd&#39;hui tu seras avec moi dans le paradis.</p>

	<p><sup class="versenum">44&nbsp;</sup>Il &eacute;tait d&eacute;j&agrave; environ la sixi&egrave;me heure, et il y eut des t&eacute;n&egrave;bres sur toute la terre, jusqu&#39;&agrave; la neuvi&egrave;me heure.</p>

	<p><sup class="versenum">45&nbsp;</sup>Le soleil s&#39;obscurcit, et le voile du temple se d&eacute;chira par le milieu.</p>

	<p><sup class="versenum">46&nbsp;</sup>J&eacute;sus s&#39;&eacute;cria d&#39;une voix forte: P&egrave;re, je remets mon esprit entre tes mains. Et, en disant ces paroles, il expira.</p>

	<p><sup class="versenum">47&nbsp;</sup>Le centenier, voyant ce qui &eacute;tait arriv&eacute;, glorifia Dieu, et dit: Certainement, cet homme &eacute;tait juste.</p>

	<p><sup class="versenum">48&nbsp;</sup>Et tous ceux qui assistaient en foule &agrave; ce spectacle, apr&egrave;s avoir vu ce qui &eacute;tait arriv&eacute;, s&#39;en retourn&egrave;rent, se frappant la poitrine.</p>

	<p><sup class="versenum">49&nbsp;</sup>Tous ceux de la connaissance de J&eacute;sus, et les femmes qui l&#39;avaient accompagn&eacute; depuis la Galil&eacute;e, se tenaient dans l&#39;&eacute;loignement et regardaient ce qui se passait.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Matthieu 27:27-56</span>;&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">27&nbsp;</sup>Les soldats du gouverneur conduisirent J&eacute;sus dans le pr&eacute;toire, et ils assembl&egrave;rent autour de lui toute la cohorte.</p>

	<p><sup class="versenum">28&nbsp;</sup>Ils lui &ocirc;t&egrave;rent ses v&ecirc;tements, et le couvrirent d&#39;un manteau &eacute;carlate.</p>

	<p><sup class="versenum">29&nbsp;</sup>Ils tress&egrave;rent une couronne d&#39;&eacute;pines, qu&#39;ils pos&egrave;rent sur sa t&ecirc;te, et ils lui mirent un roseau dans la main droite; puis, s&#39;agenouillant devant lui, ils le raillaient, en disant: Salut, roi des Juifs!</p>

	<p><sup class="versenum">30&nbsp;</sup>Et ils crachaient contre lui, prenaient le roseau, et frappaient sur sa t&ecirc;te.</p>

	<p><sup class="versenum">31&nbsp;</sup>Apr&egrave;s s&#39;&ecirc;tre ainsi moqu&eacute;s de lui, ils lui &ocirc;t&egrave;rent le manteau, lui remirent ses v&ecirc;tements, et l&#39;emmen&egrave;rent pour le crucifier.</p>

	<p><sup class="versenum">32&nbsp;</sup>Lorsqu&#39;ils sortirent, ils rencontr&egrave;rent un homme de Cyr&egrave;ne, appel&eacute; Simon, et ils le forc&egrave;rent &agrave; porter la croix de J&eacute;sus.</p>

	<p><sup class="versenum">33&nbsp;</sup>Arriv&eacute;s au lieu nomm&eacute; Golgotha, ce qui signifie lieu du cr&acirc;ne,</p>

	<p><sup class="versenum">34&nbsp;</sup>ils lui donn&egrave;rent &agrave; boire du vin m&ecirc;l&eacute; de fiel; mais, quand il l&#39;eut go&ucirc;t&eacute;, il ne voulut pas boire.</p>

	<p><sup class="versenum">35&nbsp;</sup>Apr&egrave;s l&#39;avoir crucifi&eacute;, ils se partag&egrave;rent ses v&ecirc;tements, en tirant au sort, afin que s&#39;accompl&icirc;t ce qui avait &eacute;t&eacute; annonc&eacute; par le proph&egrave;te: Ils se sont partag&eacute; mes v&ecirc;tements, et ils ont tir&eacute; au sort ma tunique.</p>

	<p><sup class="versenum">36&nbsp;</sup>Puis ils s&#39;assirent, et le gard&egrave;rent.</p>

	<p><sup class="versenum">37&nbsp;</sup>Pour indiquer le sujet de sa condamnation, on &eacute;crivit au-dessus de sa t&ecirc;te: Celui-ci est J&eacute;sus, le roi des Juifs.</p>

	<p><sup class="versenum">38&nbsp;</sup>Avec lui furent crucifi&eacute;s deux brigands, l&#39;un &agrave; sa droite, et l&#39;autre &agrave; sa gauche.</p>

	<p><sup class="versenum">39&nbsp;</sup>Les passants l&#39;injuriaient, et secouaient la t&ecirc;te,</p>

	<p><sup class="versenum">40&nbsp;</sup>en disant: Toi qui d&eacute;truis le temple, et qui le reb&acirc;tis en trois jours, sauve-toi toi-m&ecirc;me! Si tu es le Fils de Dieu, descends de la croix!</p>

	<p><sup class="versenum">41&nbsp;</sup>Les principaux sacrificateurs, avec les scribes et les anciens, se moquaient aussi de lui, et disaient:</p>

	<p><sup class="versenum">42&nbsp;</sup>Il a sauv&eacute; les autres, et il ne peut se sauver lui-m&ecirc;me! S&#39;il est roi d&#39;Isra&euml;l, qu&#39;il descende de la croix, et nous croirons en lui.</p>

	<p><sup class="versenum">43&nbsp;</sup>Il s&#39;est confi&eacute; en Dieu; que Dieu le d&eacute;livre maintenant, s&#39;il l&#39;aime. Car il a dit: Je suis Fils de Dieu.</p>

	<p><sup class="versenum">44&nbsp;</sup>Les brigands, crucifi&eacute;s avec lui, l&#39;insultaient de la m&ecirc;me mani&egrave;re.</p>

	<p><sup class="versenum">45&nbsp;</sup>Depuis la sixi&egrave;me heure jusqu&#39;&agrave; la neuvi&egrave;me, il y eut des t&eacute;n&egrave;bres sur toute la terre.</p>

	<p><sup class="versenum">46&nbsp;</sup>Et vers la neuvi&egrave;me heure, J&eacute;sus s&#39;&eacute;cria d&#39;une voix forte: &Eacute;li, &Eacute;li, lama sabachthani? c&#39;est-&agrave;-dire: Mon Dieu, mon Dieu, pourquoi m&#39;as-tu abandonn&eacute;?</p>

	<p><sup class="versenum">47&nbsp;</sup>Quelques-un de ceux qui &eacute;taient l&agrave;, l&#39;ayant entendu, dirent: Il appelle &Eacute;lie.</p>

	<p><sup class="versenum">48&nbsp;</sup>Et aussit&ocirc;t l&#39;un d&#39;eux courut prendre une &eacute;ponge, qu&#39;il remplit de vinaigre, et, l&#39;ayant fix&eacute;e &agrave; un roseau, il lui donna &agrave; boire.</p>

	<p><sup class="versenum">49&nbsp;</sup>Mais les autres disaient: Laisse, voyons si &Eacute;lie viendra le sauver.</p>

	<p><sup class="versenum">50&nbsp;</sup>J&eacute;sus poussa de nouveau un grand cri, et rendit l&#39;esprit.</p>

	<p><sup class="versenum">51&nbsp;</sup>Et voici, le voile du temple se d&eacute;chira en deux, depuis le haut jusqu&#39;en bas, la terre trembla, les rochers se fendirent,</p>

	<p><sup class="versenum">52&nbsp;</sup>les s&eacute;pulcres s&#39;ouvrirent, et plusieurs corps des saints qui &eacute;taient morts ressuscit&egrave;rent.</p>

	<p><sup class="versenum">53&nbsp;</sup>&Eacute;tant sortis des s&eacute;pulcres, apr&egrave;s la r&eacute;surrection de J&eacute;sus, ils entr&egrave;rent dans la ville sainte, et apparurent &agrave; un grand nombre de personnes.</p>

	<p><sup class="versenum">54&nbsp;</sup>Le centenier et ceux qui &eacute;taient avec lui pour garder J&eacute;sus, ayant vu le tremblement de terre et ce qui venait d&#39;arriver, furent saisis d&#39;une grande frayeur, et dirent: Assur&eacute;ment, cet homme &eacute;tait Fils de Dieu.</p>

	<p><sup class="versenum">55&nbsp;</sup>Il y avait l&agrave; plusieurs femmes qui regardaient de loin; qui avaient accompagn&eacute; J&eacute;sus depuis la Galil&eacute;e, pour le servir.</p>

	<p><sup class="versenum">56&nbsp;</sup>Parmi elles &eacute;taient Marie de Magdala, Marie, m&egrave;re de Jacques et de Joseph, et la m&egrave;re des fils de Z&eacute;b&eacute;d&eacute;e.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop4')"> Marc 15:16-41</span>.

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Les soldats conduisirent J&eacute;sus dans l&#39;int&eacute;rieur de la cour, c&#39;est-&agrave;-dire, dans le pr&eacute;toire, et ils assembl&egrave;rent toute la cohorte.</p>

	<p><sup class="versenum">17&nbsp;</sup>Ils le rev&ecirc;tirent de pourpre, et pos&egrave;rent sur sa t&ecirc;te une couronne d&#39;&eacute;pines, qu&#39;ils avaient tress&eacute;e.</p>

	<p><sup class="versenum">18&nbsp;</sup>Puis ils se mirent &agrave; le saluer: Salut, roi des Juifs!</p>

	<p><sup class="versenum">19&nbsp;</sup>Et ils lui frappaient la t&ecirc;te avec un roseau, crachaient sur lui, et, fl&eacute;chissant les genoux, ils se prosternaient devant lui.</p>

	<p><sup class="versenum">20&nbsp;</sup>Apr&egrave;s s&#39;&ecirc;tre ainsi moqu&eacute;s de lui, ils lui &ocirc;t&egrave;rent la pourpre, lui remirent ses v&ecirc;tements, et l&#39;emmen&egrave;rent pour le crucifier.</p>

	<p><sup class="versenum">21&nbsp;</sup>Ils forc&egrave;rent &agrave; porter la croix de J&eacute;sus un passant qui revenait des champs, Simon de Cyr&egrave;ne, p&egrave;re d&#39;Alexandre et de Rufus;</p>

	<p><sup class="versenum">22&nbsp;</sup>et ils conduisirent J&eacute;sus au lieu nomm&eacute; Golgotha, ce qui signifie lieu du cr&acirc;ne.</p>

	<p><sup class="versenum">23&nbsp;</sup>Ils lui donn&egrave;rent &agrave; boire du vin m&ecirc;l&eacute; de myrrhe, mais il ne le prit pas.</p>

	<p><sup class="versenum">24&nbsp;</sup>Ils le crucifi&egrave;rent, et se partag&egrave;rent ses v&ecirc;tements, en tirant au sort pour savoir ce que chacun aurait.</p>

	<p><sup class="versenum">25&nbsp;</sup>C&#39;&eacute;tait la troisi&egrave;me heure, quand ils le crucifi&egrave;rent.</p>

	<p><sup class="versenum">26&nbsp;</sup>L&#39;inscription indiquant le sujet de sa condamnation portait ces mots: Le roi des Juifs.</p>

	<p><sup class="versenum">27&nbsp;</sup>Ils crucifi&egrave;rent avec lui deux brigands, l&#39;un &agrave; sa droite, et l&#39;autre &agrave; sa gauche.</p>

	<p><sup class="versenum">28&nbsp;</sup>Ainsi fut accompli ce que dit l&#39;&Eacute;criture: Il a &eacute;t&eacute; mis au nombre des malfaiteurs.</p>

	<p><sup class="versenum">29&nbsp;</sup>Les passants l&#39;injuriaient, et secouaient la t&ecirc;te, en disant: H&eacute;! toi qui d&eacute;truis le temple, et qui le reb&acirc;tis en trois jours,</p>

	<p><sup class="versenum">30&nbsp;</sup>sauve-toi toi-m&ecirc;me, en descendant de la croix!</p>

	<p><sup class="versenum">31&nbsp;</sup>Les principaux sacrificateurs aussi, avec les scribes, se moquaient entre eux, et disaient: Il a sauv&eacute; les autres, et il ne peut se sauver lui-m&ecirc;me!</p>

	<p><sup class="versenum">32&nbsp;</sup>Que le Christ, le roi d&#39;Isra&euml;l, descende maintenant de la croix, afin que nous voyions et que nous croyions! Ceux qui &eacute;taient crucifi&eacute;s avec lui l&#39;insultaient aussi.</p>

	<p><sup class="versenum">33&nbsp;</sup>La sixi&egrave;me heure &eacute;tant venue, il y eut des t&eacute;n&egrave;bres sur toute la terre, jusqu&#39;&agrave; la neuvi&egrave;me heure.</p>

	<p><sup class="versenum">34&nbsp;</sup>Et &agrave; la neuvi&egrave;me heure, J&eacute;sus s&#39;&eacute;cria d&#39;une voix forte: &Eacute;lo&iuml;, &Eacute;lo&iuml;, lama sabachthani? ce qui signifie: Mon Dieu, mon Dieu, pourquoi m&#39;as-tu abandonn&eacute;?</p>

	<p><sup class="versenum">35&nbsp;</sup>Quelques-uns de ceux qui &eacute;taient l&agrave;, l&#39;ayant entendu, dirent: Voici, il appelle &Eacute;lie.</p>

	<p><sup class="versenum">36&nbsp;</sup>Et l&#39;un d&#39;eux courut remplir une &eacute;ponge de vinaigre, et, l&#39;ayant fix&eacute;e &agrave; un roseau, il lui donna &agrave; boire, en disant: Laissez, voyons si &Eacute;lie viendra le descendre.</p>

	<p><sup class="versenum">37&nbsp;</sup>Mais J&eacute;sus, ayant pouss&eacute; un grand cri, expira.</p>

	<p><sup class="versenum">38&nbsp;</sup>Le voile du temple se d&eacute;chira en deux, depuis le haut jusqu&#39;en bas.</p>

	<p><sup class="versenum">39&nbsp;</sup>Le centenier, qui &eacute;tait en face de J&eacute;sus, voyant qu&#39;il avait expir&eacute; de la sorte, dit: Assur&eacute;ment, cet homme &eacute;tait Fils de Dieu.</p>

	<p><sup class="versenum">40&nbsp;</sup>Il y avait aussi des femmes qui regardaient de loin. Parmi elles &eacute;taient Marie de Magdala, Marie, m&egrave;re de Jacques le mineur et de Joses, et Salom&eacute;,</p>

	<p><sup class="versenum">41&nbsp;</sup>qui le suivaient et le servaient lorsqu&#39;il &eacute;tait en Galil&eacute;e, et plusieurs autres qui &eacute;taient mont&eacute;es avec lui &agrave; J&eacute;rusalem.</p>
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

			<td class="social" @click="share('lesson', 'Leadership de la Croix: ', '/content/M2/fra/multiply2/multiply249.html')">
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