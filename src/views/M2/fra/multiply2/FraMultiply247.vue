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
                        <div class="chapter_number ltr"><h1>47.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership Serviteur</h1></div>
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
	<li>Lisez ou observez Jean 13:1-38 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 13</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Avant la f&ecirc;te de P&acirc;que, J&eacute;sus, sachant que son heure &eacute;tait venue de passer de ce monde au P&egrave;re, et ayant aim&eacute; les siens qui &eacute;taient dans le monde, mit le comble &agrave; son amour pour eux.</p>

<p><sup class="versenum">2&nbsp;</sup>Pendant le souper, lorsque le diable avait d&eacute;j&agrave; inspir&eacute; au coeur de Judas Iscariot, fils de Simon, le dessein de le livrer,</p>

<p><sup class="versenum">3&nbsp;</sup>J&eacute;sus, qui savait que le P&egrave;re avait remis toutes choses entre ses mains, qu&#39;il &eacute;tait venu de Dieu, et qu&#39;il s&#39;en allait &agrave; Dieu,</p>

<p><sup class="versenum">4&nbsp;</sup>se leva de table, &ocirc;ta ses v&ecirc;tements, et prit un linge, dont il se ceignit.</p>

<p><sup class="versenum">5&nbsp;</sup>Ensuite il versa de l&#39;eau dans un bassin, et il se mit &agrave; laver les pieds des disciples, et &agrave; les essuyer avec le linge dont il &eacute;tait ceint.</p>

<p><sup class="versenum">6&nbsp;</sup>Il vint donc &agrave; Simon Pierre; et Pierre lui dit: Toi, Seigneur, tu me laves les pieds!</p>

<p><sup class="versenum">7&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Ce que je fais, tu ne le comprends pas maintenant, mais tu le comprendras bient&ocirc;t.</p>

<p><sup class="versenum">8&nbsp;</sup>Pierre lui dit: Non, jamais tu ne me laveras les pieds. J&eacute;sus lui r&eacute;pondit: Si je ne te lave, tu n&#39;auras point de part avec moi.</p>

<p><sup class="versenum">9&nbsp;</sup>Simon Pierre lui dit: Seigneur, non seulement les pieds, mais encore les mains et la t&ecirc;te.</p>

<p><sup class="versenum">10&nbsp;</sup>J&eacute;sus lui dit: Celui qui est lav&eacute; n&#39;a besoin que de se laver les pieds pour &ecirc;tre enti&egrave;rement pur; et vous &ecirc;tes purs, mais non pas tous.</p>

<p><sup class="versenum">11&nbsp;</sup>Car il connaissait celui qui le livrait; c&#39;est pourquoi il dit: Vous n&#39;&ecirc;tes pas tous purs.</p>

<p><sup class="versenum">12&nbsp;</sup>Apr&egrave;s qu&#39;il leur eut lav&eacute; les pieds, et qu&#39;il eut pris ses v&ecirc;tements, il se remit &agrave; table, et leur dit: Comprenez-vous ce que je vous ai fait?</p>

<p><sup class="versenum">13&nbsp;</sup>Vous m&#39;appelez Ma&icirc;tre et Seigneur; et vous dites bien, car je le suis.</p>

<p><sup class="versenum">14&nbsp;</sup>Si donc je vous ai lav&eacute; les pieds, moi, le Seigneur et le Ma&icirc;tre, vous devez aussi vous laver les pieds les uns aux autres;</p>

<p><sup class="versenum">15&nbsp;</sup>car je vous ai donn&eacute; un exemple, afin que vous fassiez comme je vous ai fait.</p>

<p><sup class="versenum">16&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, le serviteur n&#39;est pas plus grand que son seigneur, ni l&#39;ap&ocirc;tre plus grand que celui qui l&#39;a envoy&eacute;.</p>

<p><sup class="versenum">17&nbsp;</sup>Si vous savez ces choses, vous &ecirc;tes heureux, pourvu que vous les pratiquiez.</p>

<p><sup class="versenum">18&nbsp;</sup>Ce n&#39;est pas de vous tous que je parle; je connais ceux que j&#39;ai choisis. Mais il faut que l&#39;&Eacute;criture s&#39;accomplisse: Celui qui mange avec moi le pain A lev&eacute; son talon contre moi.</p>

<p><sup class="versenum">19&nbsp;</sup>D&egrave;s &agrave; pr&eacute;sent je vous le dis, avant que la chose arrive, afin que, lorsqu&#39;elle arrivera, vous croyiez &agrave; ce que je suis.</p>

<p><sup class="versenum">20&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui re&ccedil;oit celui que j&#39;aurai envoy&eacute; me re&ccedil;oit, et celui qui me re&ccedil;oit, re&ccedil;oit celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">21&nbsp;</sup>Ayant ainsi parl&eacute;, J&eacute;sus fut troubl&eacute; en son esprit, et il dit express&eacute;ment: En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, l&#39;un de vous me livrera.</p>

<p><sup class="versenum">22&nbsp;</sup>Les disciples se regardaient les uns les autres, ne sachant de qui il parlait.</p>

<p><sup class="versenum">23&nbsp;</sup>Un des disciples, celui que J&eacute;sus aimait, &eacute;tait couch&eacute; sur le sein de J&eacute;sus.</p>

<p><sup class="versenum">24&nbsp;</sup>Simon Pierre lui fit signe de demander qui &eacute;tait celui dont parlait J&eacute;sus.</p>

<p><sup class="versenum">25&nbsp;</sup>Et ce disciple, s&#39;&eacute;tant pench&eacute; sur la poitrine de J&eacute;sus, lui dit: Seigneur, qui est-ce?</p>

<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus r&eacute;pondit: C&#39;est celui &agrave; qui je donnerai le morceau tremp&eacute;. Et, ayant tremp&eacute; le morceau, il le donna &agrave; Judas, fils de Simon, l&#39;Iscariot.</p>

<p><sup class="versenum">27&nbsp;</sup>D&egrave;s que le morceau fut donn&eacute;, Satan entra dans Judas. J&eacute;sus lui dit: Ce que tu fais, fais-le promptement.</p>

<p><sup class="versenum">28&nbsp;</sup>Mais aucun de ceux qui &eacute;taient &agrave; table ne comprit pourquoi il lui disait cela;</p>

<p><sup class="versenum">29&nbsp;</sup>car quelques-uns pensaient que, comme Judas avait la bourse, J&eacute;sus voulait lui dire: Ach&egrave;te ce dont nous avons besoin pour la f&ecirc;te, ou qu&#39;il lui commandait de donner quelque chose aux pauvres.</p>

<p><sup class="versenum">30&nbsp;</sup>Judas, ayant pris le morceau, se h&acirc;ta de sortir. Il &eacute;tait nuit.</p>

<p><sup class="versenum">31&nbsp;</sup>Lorsque Judas fut sorti, J&eacute;sus dit: Maintenant, le Fils de l&#39;homme a &eacute;t&eacute; glorifi&eacute;, et Dieu a &eacute;t&eacute; glorifi&eacute; en lui.</p>

<p><sup class="versenum">32&nbsp;</sup>Si Dieu a &eacute;t&eacute; glorifi&eacute; en lui, Dieu aussi le glorifiera en lui-m&ecirc;me, et il le glorifiera bient&ocirc;t.</p>

<p><sup class="versenum">33&nbsp;</sup>Mes petits enfants, je suis pour peu de temps encore avec vous. Vous me chercherez; et, comme j&#39;ai dit aux Juifs: Vous ne pouvez venir o&ugrave; je vais, je vous le dis aussi maintenant.</p>

<p><sup class="versenum">34&nbsp;</sup>Je vous donne un commandement nouveau: Aimez-vous les uns les autres; comme je vous ai aim&eacute;s, vous aussi, aimez-vous les uns les autres.</p>

<p><sup class="versenum">35&nbsp;</sup>A ceci tous conna&icirc;tront que vous &ecirc;tes mes disciples, si vous avez de l&#39;amour les uns pour les autres.</p>

<p><sup class="versenum">36&nbsp;</sup>Simon Pierre lui dit: Seigneur, o&ugrave; vas-tu? J&eacute;sus r&eacute;pondit: Tu ne peux pas maintenant me suivre o&ugrave; je vais, mais tu me suivras plus tard.</p>

<p><sup class="versenum">37&nbsp;</sup>Seigneur, lui dit Pierre, pourquoi ne puis-je pas te suivre maintenant? Je donnerai ma vie pour toi.</p>

<p><sup class="versenum">38&nbsp;</sup>J&eacute;sus r&eacute;pondit: Tu donneras ta vie pour moi! En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je te le dis, le coq ne chantera pas que tu ne m&#39;aies reni&eacute; trois fois.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/247.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 13:1-38&nbsp; </button>
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

<p>J&eacute;sus passe la derni&egrave;re semaine de Sa vie &agrave; enseignant dans le temple pendant la journ&eacute;e et &agrave; passer de temps dans la pri&egrave;re sur la Montagne des Oliviers dans la soir&eacute;e. Au cours de la derni&egrave;re nuit, il a beaucoup enseign&eacute; sur le leadership. Il met le comble &agrave; Son amour&rdquo;. IL les choque en se donnant le r&ocirc;le d&rsquo;un domestique et lave les pieds aux 12. Nul d&rsquo;entre eux n&rsquo;a fait cela! J&eacute;sus leur dit qu&rsquo;ils devraient suivre Son exemple pour s&rsquo;humilier, s&rsquo;abaisser et se server l&rsquo;un l&rsquo;autre en faisant ce qui est n&eacute;cessaire. Dans la plupart des cultures, le leadership serviteur est vu comme une faiblesse mais c&rsquo;est ainsi que le leadership fonctionne dans le Royaume de Dieu. Comme J&eacute;sus partageait le dernier souper avec son &eacute;quipe de base la plus proche compos&eacute;e des 12, il &eacute;tait attrist&eacute; sachant que l&#39;un d&#39;eux le trahirait. Judas &eacute;tait d&eacute;sillusionn&eacute; par le leadership de J&eacute;sus et avait d&eacute;j&agrave; conclu un accord pour aider les chefs religieux &agrave; arr&ecirc;ter J&eacute;sus dans un endroit calme, loin des foules. Judas s&#39;est ouvert pour &ecirc;tre manipul&eacute; par Satan, le vieil ennemi de J&eacute;sus. Dans ce contexte, J&eacute;sus recommande aux disciples de s&#39;aimer les uns les autres.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 22:7-38</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>Le jour des pains sans levain, o&ugrave; l&#39;on devait immoler la P&acirc;que, arriva,</p>

	<p><sup class="versenum">8&nbsp;</sup>et J&eacute;sus envoya Pierre et Jean, en disant: Allez nous pr&eacute;parer la P&acirc;que, afin que nous la mangions.</p>

	<p><sup class="versenum">9&nbsp;</sup>Ils lui dirent: O&ugrave; veux-tu que nous la pr&eacute;parions?</p>

	<p><sup class="versenum">10&nbsp;</sup>Il leur r&eacute;pondit: Voici, quand vous serez entr&eacute;s dans la ville, vous rencontrerez un homme portant une cruche d&#39;eau; suivez-le dans la maison o&ugrave; il entrera,</p>

	<p><sup class="versenum">11&nbsp;</sup>et vous direz au ma&icirc;tre de la maison: Le ma&icirc;tre te dit: O&ugrave; est le lieu o&ugrave; je mangerai la P&acirc;que avec mes disciples?</p>

	<p><sup class="versenum">12&nbsp;</sup>Et il vous montrera une grande chambre haute, meubl&eacute;e: c&#39;est l&agrave; que vous pr&eacute;parerez la P&acirc;que.</p>

	<p><sup class="versenum">13&nbsp;</sup>Ils partirent, et trouv&egrave;rent les choses comme il le leur avait dit; et ils pr&eacute;par&egrave;rent la P&acirc;que.</p>

	<p><sup class="versenum">14&nbsp;</sup>L&#39;heure &eacute;tant venue, il se mit &agrave; table, et les ap&ocirc;tres avec lui.</p>

	<p><sup class="versenum">15&nbsp;</sup>Il leur dit: J&#39;ai d&eacute;sir&eacute; vivement manger cette P&acirc;que avec vous, avant de souffrir;</p>

	<p><sup class="versenum">16&nbsp;</sup>car, je vous le dis, je ne la mangerai plus, jusqu&#39;&agrave; ce qu&#39;elle soit accomplie dans le royaume de Dieu.</p>

	<p><sup class="versenum">17&nbsp;</sup>Et, ayant pris une coupe et rendu gr&acirc;ces, il dit: Prenez cette coupe, et distribuez-la entre vous;</p>

	<p><sup class="versenum">18&nbsp;</sup>car, je vous le dis, je ne boirai plus d&eacute;sormais du fruit de la vigne, jusqu&#39;&agrave; ce que le royaume de Dieu soit venu.</p>

	<p><sup class="versenum">19&nbsp;</sup>Ensuite il prit du pain; et, apr&egrave;s avoir rendu gr&acirc;ces, il le rompit, et le leur donna, en disant: Ceci est mon corps, qui est donn&eacute; pour vous; faites ceci en m&eacute;moire de moi.</p>

	<p><sup class="versenum">20&nbsp;</sup>Il prit de m&ecirc;me la coupe, apr&egrave;s le souper, et la leur donna, en disant: Cette coupe est la nouvelle alliance en mon sang, qui est r&eacute;pandu pour vous.</p>

	<p><sup class="versenum">21&nbsp;</sup>Cependant voici, la main de celui qui me livre est avec moi &agrave; cette table.</p>

	<p><sup class="versenum">22&nbsp;</sup>Le Fils de l&#39;homme s&#39;en va selon ce qui est d&eacute;termin&eacute;. Mais malheur &agrave; l&#39;homme par qui il est livr&eacute;!</p>

	<p><sup class="versenum">23&nbsp;</sup>Et ils commenc&egrave;rent &agrave; se demander les uns aux autres qui &eacute;tait celui d&#39;entre eux qui ferait cela.</p>

	<p><sup class="versenum">24&nbsp;</sup>Il s&#39;&eacute;leva aussi parmi les ap&ocirc;tres une contestation: lequel d&#39;entre eux devait &ecirc;tre estim&eacute; le plus grand?</p>

	<p><sup class="versenum">25&nbsp;</sup>J&eacute;sus leur dit: Les rois des nations les ma&icirc;trisent, et ceux qui les dominent sont appel&eacute;s bienfaiteurs.</p>

	<p><sup class="versenum">26&nbsp;</sup>Qu&#39;il n&#39;en soit pas de m&ecirc;me pour vous. Mais que le plus grand parmi vous soit comme le plus petit, et celui qui gouverne comme celui qui sert.</p>

	<p><sup class="versenum">27&nbsp;</sup>Car quel est le plus grand, celui qui est &agrave; table, ou celui qui sert? N&#39;est-ce pas celui qui est &agrave; table? Et moi, cependant, je suis au milieu de vous comme celui qui sert.</p>

	<p><sup class="versenum">28&nbsp;</sup>Vous, vous &ecirc;tes ceux qui avez pers&eacute;v&eacute;r&eacute; avec moi dans mes &eacute;preuves;</p>

	<p><sup class="versenum">29&nbsp;</sup>c&#39;est pourquoi je dispose du royaume en votre faveur, comme mon P&egrave;re en a dispos&eacute; en ma faveur,</p>

	<p><sup class="versenum">30&nbsp;</sup>afin que vous mangiez et buviez &agrave; ma table dans mon royaume, et que vous soyez assis sur des tr&ocirc;nes, pour juger les douze tribus d&#39;Isra&euml;l.</p>

	<p><sup class="versenum">31&nbsp;</sup>Le Seigneur dit: Simon, Simon, Satan vous a r&eacute;clam&eacute;s, pour vous cribler comme le froment.</p>

	<p><sup class="versenum">32&nbsp;</sup>Mais j&#39;ai pri&eacute; pour toi, afin que ta foi ne d&eacute;faille point; et toi, quand tu seras converti, affermis tes fr&egrave;res.</p>

	<p><sup class="versenum">33&nbsp;</sup>Seigneur, lui dit Pierre, je suis pr&ecirc;t &agrave; aller avec toi et en prison et &agrave; la mort.</p>

	<p><sup class="versenum">34&nbsp;</sup>Et J&eacute;sus dit: Pierre, je te le dis, le coq ne chantera pas aujourd&#39;hui que tu n&#39;aies ni&eacute; trois fois de me conna&icirc;tre.</p>

	<p><sup class="versenum">35&nbsp;</sup>Il leur dit encore: Quand je vous ai envoy&eacute;s sans bourse, sans sac, et sans souliers, avez-vous manqu&eacute; de quelque chose? Ils r&eacute;pondirent: De rien.</p>

	<p><sup class="versenum">36&nbsp;</sup>Et il leur dit: Maintenant, au contraire, que celui qui a une bourse la prenne et que celui qui a un sac le prenne &eacute;galement, que celui qui n&#39;a point d&#39;&eacute;p&eacute;e vende son v&ecirc;tement et ach&egrave;te une &eacute;p&eacute;e.</p>

	<p><sup class="versenum">37&nbsp;</sup>Car, je vous le dis, il faut que cette parole qui est &eacute;crite s&#39;accomplisse en moi: Il a &eacute;t&eacute; mis au nombre des malfaiteurs. Et ce qui me concerne est sur le point d&#39;arriver.</p>

	<p><sup class="versenum">38&nbsp;</sup>Ils dirent: Seigneur, voici deux &eacute;p&eacute;es. Et il leur dit: Cela suffit.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Matthieu 26:17-29</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">17&nbsp;</sup>Le premier jour des pains sans levain, les disciples s&#39;adress&egrave;rent &agrave; J&eacute;sus, pour lui dire: O&ugrave; veux-tu que nous te pr&eacute;parions le repas de la P&acirc;que?</p>

	<p><sup class="versenum">18&nbsp;</sup>Il r&eacute;pondit: Allez &agrave; la ville chez un tel, et vous lui direz: Le ma&icirc;tre dit: Mon temps est proche; je ferai chez toi la P&acirc;que avec mes disciples.</p>

	<p><sup class="versenum">19&nbsp;</sup>Les disciples firent ce que J&eacute;sus leur avait ordonn&eacute;, et ils pr&eacute;par&egrave;rent la P&acirc;que.</p>

	<p><sup class="versenum">20&nbsp;</sup>Le soir &eacute;tant venu, il se mit &agrave; table avec les douze.</p>

	<p><sup class="versenum">21&nbsp;</sup>Pendant qu&#39;ils mangeaient, il dit: Je vous le dis en v&eacute;rit&eacute;, l&#39;un de vous me livrera.</p>

	<p><sup class="versenum">22&nbsp;</sup>Ils furent profond&eacute;ment attrist&eacute;s, et chacun se mit &agrave; lui dire: Est-ce moi, Seigneur?</p>

	<p><sup class="versenum">23&nbsp;</sup>Il r&eacute;pondit: Celui qui a mis avec moi la main dans le plat, c&#39;est celui qui me livrera.</p>

	<p><sup class="versenum">24&nbsp;</sup>Le Fils de l&#39;homme s&#39;en va, selon ce qui est &eacute;crit de lui. Mais malheur &agrave; l&#39;homme par qui le Fils de l&#39;homme est livr&eacute;! Mieux vaudrait pour cet homme qu&#39;il ne f&ucirc;t pas n&eacute;.</p>

	<p><sup class="versenum">25&nbsp;</sup>Judas, qui le livrait, prit la parole et dit: Est-ce moi, Rabbi? J&eacute;sus lui r&eacute;pondit: Tu l&#39;as dit.</p>

	<p><sup class="versenum">26&nbsp;</sup>Pendant qu&#39;ils mangeaient, J&eacute;sus prit du pain; et, apr&egrave;s avoir rendu gr&acirc;ces, il le rompit, et le donna aux disciples, en disant: Prenez, mangez, ceci est mon corps.</p>

	<p><sup class="versenum">27&nbsp;</sup>Il prit ensuite une coupe; et, apr&egrave;s avoir rendu gr&acirc;ces, il la leur donna, en disant: Buvez-en tous;</p>

	<p><sup class="versenum">28&nbsp;</sup>car ceci est mon sang, le sang de l&#39;alliance, qui est r&eacute;pandu pour plusieurs, pour la r&eacute;mission des p&eacute;ch&eacute;s.</p>

	<p><sup class="versenum">29&nbsp;</sup>Je vous le dis, je ne boirai plus d&eacute;sormais de ce fruit de la vigne, jusqu&#39;au jour o&ugrave; j&#39;en boirai du nouveau avec vous dans le royaume de mon P&egrave;re.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop3')"> Marc 14:12-25</span>.

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>Le premier jour des pains sans levain, o&ugrave; l&#39;on immolait la P&acirc;que, les disciples de J&eacute;sus lui dirent: O&ugrave; veux-tu que nous allions te pr&eacute;parer la P&acirc;que?</p>

	<p><sup class="versenum">13&nbsp;</sup>Et il envoya deux de ses disciples, et leur dit: Allez &agrave; la ville; vous rencontrerez un homme portant une cruche d&#39;eau, suivez-le.</p>

	<p><sup class="versenum">14&nbsp;</sup>Quelque part qu&#39;il entre, dites au ma&icirc;tre de la maison: Le ma&icirc;tre dit: O&ugrave; est le lieu o&ugrave; je mangerai la P&acirc;que avec mes disciples?</p>

	<p><sup class="versenum">15&nbsp;</sup>Et il vous montrera une grande chambre haute, meubl&eacute;e et toute pr&ecirc;te: c&#39;est l&agrave; que vous nous pr&eacute;parerez la P&acirc;que.</p>

	<p><sup class="versenum">16&nbsp;</sup>Les disciples partirent, arriv&egrave;rent &agrave; la ville, et trouv&egrave;rent les choses comme il le leur avait dit; et ils pr&eacute;par&egrave;rent la P&acirc;que.</p>

	<p><sup class="versenum">17&nbsp;</sup>Le soir &eacute;tant venu, il arriva avec les douze.</p>

	<p><sup class="versenum">18&nbsp;</sup>Pendant qu&#39;ils &eacute;taient &agrave; table et qu&#39;ils mangeaient, J&eacute;sus dit: Je vous le dis en v&eacute;rit&eacute;, l&#39;un de vous, qui mange avec moi, me livrera.</p>

	<p><sup class="versenum">19&nbsp;</sup>Ils commenc&egrave;rent &agrave; s&#39;attrister, et &agrave; lui dire, l&#39;un apr&egrave;s l&#39;autre: Est-ce moi?</p>

	<p><sup class="versenum">20&nbsp;</sup>Il leur r&eacute;pondit: C&#39;est l&#39;un des douze, qui met avec moi la main dans le plat.</p>

	<p><sup class="versenum">21&nbsp;</sup>Le Fils de l&#39;homme s&#39;en va selon ce qui est &eacute;crit de lui. Mais malheur &agrave; l&#39;homme par qui le Fils de l&#39;homme est livr&eacute;! Mieux vaudrait pour cet homme qu&#39;il ne f&ucirc;t pas n&eacute;.</p>

	<p><sup class="versenum">22&nbsp;</sup>Pendant qu&#39;ils mangeaient, J&eacute;sus prit du pain; et, apr&egrave;s avoir rendu gr&acirc;ces, il le rompit, et le leur donna, en disant: Prenez, ceci est mon corps.</p>

	<p><sup class="versenum">23&nbsp;</sup>Il prit ensuite une coupe; et, apr&egrave;s avoir rendu gr&acirc;ces, il la leur donna, et ils en burent tous.</p>

	<p><sup class="versenum">24&nbsp;</sup>Et il leur dit: Ceci est mon sang, le sang de l&#39;alliance, qui est r&eacute;pandu pour plusieurs.</p>

	<p><sup class="versenum">25&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;, je ne boirai plus jamais du fruit de la vigne, jusqu&#39;au jour o&ugrave; je le boirai nouveau dans le royaume de Dieu.</p>
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

			<td class="social" @click="share('lesson', 'Leadership Serviteur: ', '/content/M2/fra/multiply2/multiply247.html')">
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