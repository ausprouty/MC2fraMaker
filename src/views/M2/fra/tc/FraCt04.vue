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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-tc-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>4.</h1></div>
                        <div class="chapter_title ltr"><h1>Comment marcher par l'Esprit</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p><em>Chuck appuya une fois encore sur le klaxon, un long coup empreint de col&egrave;re. Voici d&eacute;j&agrave; dix minutes qu&rsquo;il attendait. O&ugrave; &eacute;taient-ils? Marianne savait combien nerveux il &eacute;tait ce matin, son premier dimanche o&ugrave; il devait enseigner les gar&ccedil;ons de 10-11 ans. Il avait demand&eacute; aux enfants et elle d&rsquo;&ecirc;tre &agrave; l&rsquo;heure&nbsp;! Enfin elle arriva, ouvrit la porte et aida celui de 3 ans &agrave; entrer dans la voiture. </em><br />
<br />
<em>&laquo;&nbsp;Je ne peux pas y croire&nbsp;&raquo;, hurla Chuck quand la petite Julie de 6 ans se blottissait dans le coin du si&egrave;ge arri&egrave;re. &laquo;&nbsp;Je vous ai dit que je devrais &ecirc;tre l&agrave;-bas t&ocirc;t. Je dois aligner les chaises et appr&ecirc;ter les mat&eacute;riels&nbsp;!&nbsp;&raquo; </em><br />
<br />
<em>Marianne tenta faiblement de s&rsquo;excuser pendant qu&rsquo;ils sortaient de la vons et se dirigeaient &ndash;en vitesse -&nbsp; vers l&rsquo;&eacute;glise. Chuck continuait &agrave; temp&ecirc;ter sur sa famille sans la moindre consid&eacute;ration du sentiment de cette derni&egrave;re &hellip; jusqu&rsquo;&agrave; ce que quelque chose au fond de son &ecirc;tre sembla lui dire, Tu es dans un parfait &eacute;tait d&rsquo;esprit pour enseigner au sujet de l&rsquo;amour de Dieu et de la patience, n&rsquo;est-ce pas&nbsp;? Il reconnut la &laquo;&nbsp;voix&nbsp;&raquo; en un instant. Elle parla calmement au milieu de sa col&egrave;re et, comme toujours, toucha directement le c&oelig;ur du probl&egrave;me. Il ne pouvait pas discuter; il savait que la voix avait raison. </em><br />
<br />
<em>Il jeta un coup d&rsquo;&oelig;il &agrave; son &eacute;pouse. Juste quelques secondes plus t&ocirc;t, il avait &eacute;t&eacute; si f&acirc;ch&eacute; qu&rsquo;il l&rsquo;avait vu comme un ennemi. Maintenant, ce qu&rsquo;il a vu, c&rsquo;est la femme qu&rsquo;elle aimait, qui regardait tristement par la fen&ecirc;tre &agrave; mesure que les maisons glissaient et passaient &agrave; c&ocirc;t&eacute; d&rsquo;eux. Il l&rsquo;avait profond&eacute;ment bless&eacute;e avec son coup de col&egrave;re. </em><br />
<br />
<em>&ldquo;Ch&eacute;rie,&rdquo; dit-il en touchant sa main, &ldquo;je te dois des excuses&rdquo; Au cours du reste du voyage, ils parlaient calmement ensemble pensant les sentiments du c&oelig;ur,&nbsp; r&eacute;parant les injustices, et restaurant leur communication. </em><br />
<br />
Chuck a rechut&eacute; dans les pratiques de l&rsquo;&rdquo;homme charnel&rdquo; comme tous autant que nous sommes le faisons de temps en temps. Il a &eacute;t&eacute; si impliqu&eacute; dans le probl&egrave;me du moment qu&rsquo;il a oubli&eacute; celui qui devrait &ecirc;tre sur le tr&ocirc;ne de sa vie. Retourner &agrave; notre &agrave; notre voie charnelle je le ferai moi-m&ecirc;me est presqu&rsquo;un r&eacute;flexe quand nous oublions de croire les promesses de la Parole de Dieu (Jean 1&nbsp;:9) et leurs provisions dans notre vie quotidienne. Nous oublions 1 Corinthiens 10&nbsp;:13&nbsp;? &laquo;&nbsp;Aucune tentation ne vous est survenue qui n&#39;ait &eacute;t&eacute; humaine, et Dieu, qui est fid&egrave;le, ne permettra pas que vous soyez tent&eacute;s au del&agrave; de vos forces; mais avec la tentation il pr&eacute;parera aussi le moyen d&#39;en sortir, afin que vous puissiez la supporter.&nbsp;&raquo; &nbsp;<br />
<br />
Paul dit dans Romains 14&nbsp;: 23 &laquo;&nbsp;Tout ce qui n&#39;est pas le produit d&#39;une conviction est p&eacute;ch&eacute;.&nbsp;&raquo; Ce n&rsquo;est pas le p&eacute;ch&eacute; lui-m&ecirc;me qui nous retourne &agrave; l&rsquo;&eacute;tat charnel &agrave; nouveau, c&rsquo;est ce que nous d&eacute;cidons de faire au sujet de ce p&eacute;ch&eacute;. Si nous arr&ecirc;tons de respirer spirituellement et permettons au p&eacute;ch&eacute; de nous s&eacute;parer de Dieu et/ou notre croyance en Sa puissance pour nos vies, notre seul choix est de vivre une fois encore comme des Chr&eacute;tiens charnels.&nbsp; D&rsquo;autre part, lorsque nous choisissons de respirer spirituellement &ndash; confessant nos p&eacute;ch&eacute;s &agrave; Dieu moment apr&egrave;s moment (expiration), et respirer profond&eacute;ment de Son pardon et sa restauration (inspiration)&nbsp; - nous continuons de le maintenir sur le tr&ocirc;ne et de vivre une vie victorieuse.<br />
<br />
Pendant que Chuck conduisait sa famille &agrave; l&rsquo;&eacute;glise ce dimanche matin,&nbsp; il &laquo;&nbsp;expira&nbsp;&raquo;&nbsp; lorsqu&rsquo;il confessa son p&eacute;ch&eacute; &agrave; Dieu et &agrave; sa famille. Et il&nbsp; &laquo;&nbsp;inspira&nbsp;&raquo; une fra&icirc;che onction du Saint Esprit lorsqu&rsquo;il ouvra une fois encore son c&oelig;ur &agrave; la Puissance restauratrice de Dieu et r&eacute;gla les choses avec son &eacute;pouse. Lorsqu&rsquo;il se tenait debout devant ces gar&ccedil;ons de 10-11 ans, il &eacute;tait pr&ecirc;t &agrave; leur parler avec conviction de l&rsquo;amour inconditionnel de Dieu pour nous en tant que Ses enfants qu&rsquo;il a rachet&eacute;s. Les gar&ccedil;ons ont senti en leur moniteur une humilit&eacute; et une honn&ecirc;tet&eacute; qui les ont conduits au Sauveur. Et avant la fin du cours, trois d&rsquo;entre les enfants ont donn&eacute; leur c&oelig;ur &agrave; Dieu. Le Seigneur Se donne gloire &agrave; travers les vies consacr&eacute;es de Ses enfants.<br />
<br />
Lorsque vous &laquo;&nbsp;expirez&nbsp;&raquo; et &laquo;&nbsp;inspirez&nbsp;&raquo; spirituellement, vous remarquerez une diff&eacute;rence dans votre vie. Vous deviendrez &laquo;&nbsp;spirituellement au point&nbsp;&raquo; et vous remarquerez une nouvelle libert&eacute; et une nouvelle puissance dans votre t&eacute;moignage.&nbsp; Quand le p&eacute;ch&eacute; fait son entr&eacute;e, ne lui permettez pas de vous retenir en arri&egrave;re.&nbsp; R&eacute;glez simplement vos comptes avec Dieu le plus t&ocirc;t possible et ne permettez pas au p&eacute;ch&eacute; de s&rsquo;accumuler. Jean &eacute;crit &laquo; &nbsp;Mes petits enfants, je vous &eacute;cris ces choses, afin que vous ne p&eacute;chiez point. Et si quelqu&#39;un a p&eacute;ch&eacute;, nous avons un avocat aupr&egrave;s du P&egrave;re, J&eacute;sus Christ le juste.&nbsp;&raquo; 1 Jean 2&nbsp;: 1-2 LSG<br />
<br />
A mesure que votre relation avec le Saint Esprit murit, vous d&eacute;couvrirez qu&rsquo;elle est &agrave; la fois critique et progressive. Elle est critique en ce que, &agrave; mesure que vous continuez &agrave; vous approprier Sa puissance moment apr&egrave;s moment, vous apprendrez comment vous approprier par la foi ce qu&rsquo;Il vous offre. Votre&nbsp; relation est progressive en ce que, par la foi, vous grandirez et deviendrez mature dans votre vie dirig&eacute;e par l&rsquo;Esprit. Il est souvent facile d&rsquo;identifier un croyant qui a march&eacute; par l&rsquo;Esprit des ann&eacute;es durant parce que le fruit de l&rsquo;Esprit est facilement visible (dans sa vie).<br />
<br />
Le concept de &laquo;&nbsp;la respiration spirituelle&nbsp;&raquo; n&rsquo;en est pas un de complexe, mais il a besoin d&rsquo;&ecirc;tre compris dans un contexte plus large. Il y a quatre choses au sujet desquelles nous devons prendre des pr&eacute;cautions dans notre marche chr&eacute;tienne&nbsp;:</p>

<p>&nbsp;</p>

<ol>
	<li>&Ecirc;tre certain que nous sommes remplis du Saint Esprit.</li>
	<li>Se pr&eacute;parer pour le conflit spirituel.</li>
	<li>Conna&icirc;tre nos droits en tant qu&rsquo;enfants de Dieu.</li>
	<li>Vivre par la foi.</li>
</ol>

<p>&nbsp;</p>

<h2>&Ecirc;tre rempli du Saint Esprit</h2>

<p>En premier, afin de marcher par l&rsquo;Esprit, nous devons nous assurer de ce que nous sommes remplis de l&rsquo;Esprit. Dans Eph&eacute;siens 5&nbsp;: 18 il nous est dit&nbsp;: &laquo;&nbsp;&nbsp;Ne vous enivrez pas de vin: c&#39;est de la d&eacute;bauche. Soyez, au contraire, remplis de l&#39;Esprit&nbsp;&raquo; (LSG).&nbsp; &Ecirc;tre rempli de l&rsquo;Esprit Saint c&rsquo;est &ecirc;tre dirig&eacute; et habilit&eacute; par Lui comme un mode de vie. J&eacute;sus avertit, &laquo;&nbsp;Nul ne peut servir deux ma&icirc;tres. Car, ou il ha&iuml;ra l&#39;un, et aimera l&#39;autre; ou il s&#39;attachera &agrave; l&#39;un, et m&eacute;prisera l&#39;autre. Vous ne pouvez servir Dieu et Mamon.&nbsp;&raquo;&nbsp; (Matthieu 6:24)<br />
<br />
Il y a un &ldquo;tr&ocirc;ne&rdquo; dans chaque c&oelig;ur &ndash; notre centre de contr&ocirc;le &ndash;et il n&rsquo;y de place sur le tr&ocirc;ne qu&rsquo;une seule puissance qui r&egrave;gne. La lutte se passe autour du contr&ocirc;le de ce tr&ocirc;ne.&nbsp; Et le Chr&eacute;tien qui est dirig&eacute; par le moi a enlev&eacute; le Saint Esprit du tr&ocirc;ne de leur vie.<br />
<br />
Il est imp&eacute;ratif que nous rappelions le commandement de Dieu pour nous et Sa promesse. Il nous commande d&rsquo;&nbsp;&laquo;&nbsp;&Ecirc;tre rempli&nbsp;&raquo;. Il promet que si nous demandons quelque chose selon la volont&eacute; de Dieu, il entendra et r&eacute;pondra (1Jean 5&nbsp;:15-15). Parce qu&rsquo;il nous commande d&rsquo;&ecirc;tre remplis du Saint,&nbsp; nous pouvons &ecirc;tre s&ucirc;rs que si nous demandons quelque chose qui est dans Sa volont&eacute; pour nos vies. Et quand nous prions selon Sa volont&eacute;, Il a promis de r&eacute;pondre &agrave; nos requ&ecirc;tes.<br />
<br />
En cons&eacute;quence, nous pouvons esp&eacute;rer qu&rsquo;Il nous remplisse et nous habilite quand nous d&eacute;sirons sinc&egrave;rement de soumettre le contr&ocirc;le de nos vies &agrave; Lui, et Lui faisons confiance pour qu&rsquo;Il nous remplisse de Son Esprit. Ensuite, nous devons continuer &agrave; respirer spirituellement, &laquo;&nbsp;expirant&nbsp;&raquo; en confessant et &laquo;&nbsp;inspirant&nbsp;&raquo; en nous appropriant Son pardon et sa puissance dans nos vies&nbsp; par la foi.<br />
<br />
Qu&rsquo;en est-il des &eacute;motions dans l&rsquo;exp&eacute;rience du croyant?<br />
<br />
Les sentiments ajoutent de la coloration et de la joie et font une partie importante de la vie, mais ils sont extr&ecirc;mement inconstants, changeant avec l&rsquo;atmosph&egrave;re. En tant que chr&eacute;tiens, nous vivons par la foi, en faisant confiance &agrave; la fid&eacute;lit&eacute; de Dieu et aux promesses de sa Parole Si nous d&eacute;pendons des sentiments pour la confirmation de Son &oelig;uvre dans nos vies, nous nous mettons dans une dangereuse position et seront presque toujours d&eacute;&ccedil;us.<br />
<br />
Comparons le processus de croire en Dieu et vivre la vie chr&eacute;tienne &agrave; un train. La puissance est dans le moteur (FAIT), le carburant est dans le wagon &agrave; charbon (FOI) et ce qui ferme la marche est le fourgon de queue (LES SENTIMENTS). Aucun ing&eacute;nieur n&rsquo;accrochera son train &agrave; un fourgon de queue pour esp&eacute;rer qu&rsquo;il tire la charge. Le moteur - fait &ndash; donne au christianisme sa puissance, et souvent les <em>sentiments</em> s&rsquo;en suivent naturellement, comme un bonus. Mais s&rsquo;ils ne sont pas l&agrave;, cela ne veut pas dire que les faits ont chang&eacute;.<br />
<br />
Refusez de rechercher les exp&eacute;riences &eacute;motionnelles comme une preuve de la pr&eacute;sence permanente du Saint Esprit en vous. Si vous avez une faim et une soif sinc&egrave;re de la justice de Dieu, et vous avez confess&eacute; vos p&eacute;ch&eacute;s, vous vous &ecirc;tes soumis &agrave; Sa direction, et vous Lui avez demand&eacute; de vous remplir, vous pouvez &ecirc;tre assur&eacute; que <em>vous &ecirc;tes remplis du Saint Esprit&nbsp;!</em> Dieu est fid&egrave;le &agrave; Ses promesses.<br />
<br />
Jean 14:21 nous rappelle, &laquo;&nbsp;Celui qui a mes commandements et qui les garde, c&#39;est celui qui m&#39;aime; et celui qui m&#39;aime sera aim&eacute; de mon P&egrave;re, je l&#39;aimerai, et je me ferai conna&icirc;tre &agrave; lui&nbsp;&raquo;. Il ne dit pas, &laquo;&nbsp;Celui qui ressent de l&rsquo;amour pour moi,&nbsp;&raquo; mais &laquo;&nbsp;Celui qui garde mes commandements &raquo;.<br />
<br />
Les sentiments suivent d&rsquo;habitudes les d&eacute;cisions et les actions de nos vies, mais nous n&rsquo;avons pas besoin de les rechercher encore moins de d&eacute;pendre d&rsquo;eux pour nous confirmer des faits. Rechercher une exp&eacute;rience &eacute;motionnelle c&rsquo;est une d&eacute;n&eacute;gation du concept de la foi, et tout ce qui n&rsquo;est pas de la foi est un p&eacute;ch&eacute; (H&eacute;breux 11&nbsp;:6). Quand nous croyons en Dieu, il honore notre foi, et nous pouvons vivre la vie avec l&rsquo;assurance qu&rsquo;Il nous remplit moment apr&egrave;s moment.</p>

<h2>&Ecirc;tre Pr&ecirc;t pour le Conflit Spirituel</h2>

<p>En second lieu, comme tous bons soldats pr&eacute;par&eacute;s pour le combat, nous devons <em>&ecirc;tre pr&ecirc;ts pour le conflit spirituel</em>. Nous qui avons choisi d&rsquo;&ecirc;tre spirituellement vivant et attach&eacute; &agrave; notre Seigneur, devons esp&eacute;rer une r&eacute;sistance de la part de l&rsquo;ennemi. Et l&rsquo;une des armes les plus tranchantes de l&rsquo;ennemi c&rsquo;est la culpabilit&eacute;. Il piquera quand nous nous y attendrons le moins avec les piqures d&rsquo;&eacute;pines de grande ortie qui causent d&eacute;mangeaisons et gonflements. Il nous accusera des p&eacute;ch&eacute;s pour lesquels nous avons d&eacute;j&agrave; accept&eacute; le pardon de Dieu, et il fera tout ce qui est possible pour d&eacute;truire notre s&eacute;curit&eacute; en Christ,&nbsp; car l&rsquo;ennemie sait qu&rsquo;un soldat qui doute est sans importance dans une bataille:</p>

<ul>
	<li>Ne permettez pas &agrave; Satan de braquer son arc. Un &laquo;&nbsp;cible en mouvement&nbsp;&raquo; est toujours plus difficile &agrave; atteindre.</li>
	<li>Refusez de rechuter dans une introspection non n&eacute;cessaire (l&rsquo;une des ruses favorites de Satan). Ceci vous emp&ecirc;chera &agrave; faire des incursions dans zones qui ont d&eacute;j&agrave; &eacute;t&eacute; pardonn&eacute;s et oubli&eacute;s par le Sauveur&nbsp;!</li>
	<li>Ne confessez &agrave; Dieu que ce dont le Saint Esprit donne l&rsquo;impression dans votre c&oelig;ur comme &eacute;tant quelque chose qui se tient debout entre vous et sa pl&eacute;nitude dans votre c&oelig;ur.</li>
	<li>Il nous est dit dans 1 Pierre 5: 7-8 de de nous d&eacute;charger sur Dieu de tous nos soucis car il est toujours en train de penser &agrave; nous et de veiller sur tout ce qui nous concerne. Nous devons faire attention &ndash; et pr&ecirc;t pour les attaques in&eacute;vitables de Satan, le grand ennemi, qui r&ocirc;des sur la terre comme un lion rugissant cherchant la prochaine victime &agrave; d&eacute;chirer. Il est un adversaire malin et impitoyable qui attaque soit de fa&ccedil;on subtile ou &agrave; visage d&eacute;couvert, et essaye de nous vaincre et de nous d&eacute;truire. Mais nous pouvons &ecirc;tre confiant que &laquo;&nbsp;Celui qui est en vous est plus grand que celui qui est dans le monde&nbsp;&raquo; (1 Jean 4&nbsp;:4).</li>
</ul>

<p>Il y a deux mille ans, Satan a &eacute;t&eacute; vaincu lorsque J&eacute;sus Christ est mort sur la croix pour nos p&eacute;ch&eacute;s. La victoire est pour nous maintenant! Nous ne regardons pas devant pour la victoire, mais plut&ocirc;t derri&egrave;re &agrave; la croix o&ugrave; l&rsquo;ennemi a &eacute;t&eacute; vaincu une fois pour toute. Nous n&rsquo;avons pas besoin de craindre Satan aussi longtemps que nous marchons par l&rsquo;Esprit et d&eacute;pendons de Christ pour notre force et notre provision.&nbsp; &nbsp;</p>

<h2>Connaissez vos droits en tant qu&rsquo;Enfants de Dieu</h2>

<p>Troisi&egrave;mement, si nous devons constamment marcher par l&rsquo;Esprit, nous devons connaitre quels sont nos droits en tant qu&rsquo;enfants de Dieu (Jean 1&nbsp;:12). Nous avons h&eacute;rit&eacute; d&rsquo;une provision intarissable d&rsquo;amour, de puissance, de pardon, et de gr&acirc;ce de la part de notre P&egrave;re. Il est de notre responsabilit&eacute; d&rsquo;apprendre comment utiliser cette provision.<br />
<br />
Le livre source qui d&eacute;clare nos droits d&rsquo;h&eacute;ritage est bien la Bible. En tant que croyants, nous devons passer du temps &agrave; lire, &eacute;tudier, m&eacute;moriser, et m&eacute;diter la Parole de Dieu pour vivre d&rsquo;une fa&ccedil;on qui Lui plaira. Les d&eacute;sirs de Son c&oelig;ur pour nous, ces pr&eacute;cieux enfants, sont cach&eacute;s dans les Ecritures.&nbsp; Lorsque nous recherchons ces v&eacute;rit&eacute;s, elles nous sont r&eacute;v&eacute;l&eacute;es par le Saint Esprit Lui-m&ecirc;me.<br />
<br />
Par exemple, quand Christ &eacute;tablit sa demeure en nos vies, nos corps deviennent Ses temples vivants.&nbsp; J&eacute;sus nous a promis Sa puissance sp&eacute;ciale pour vivre des vies saintes (Romains 12:1-2). En tant que ses enfants, c&rsquo;est une chose dont nous avons h&eacute;rit&eacute;.<br />
<br />
Nous pouvons aussi &ecirc;tre des t&eacute;moins efficaces de Lui. Quand Son Esprit nous dirige, nous sommes remplis de Son amour pour les perdus. Et pendant que nous partageons la v&eacute;rit&eacute; avec eux, Il parle &agrave; travers nous. &nbsp;<br />
<br />
Un mot d&rsquo;avertissement&nbsp;: Nous devons faire attention &agrave; ne pas penser &agrave; l&rsquo;&eacute;tude biblique, la pri&egrave;re, et le t&eacute;moignage comme &ldquo;les &oelig;uvres&rdquo; qui justifient notre position en Christ. En v&eacute;rit&eacute;, c&rsquo;est juste le contraire. Les &oelig;uvres que nous faisons au nom de notre Seigneur sont les r&eacute;sultats de ce que nous vivons pour plaire au Sauveur.&nbsp; Et les r&eacute;sultats sont la preuve d&rsquo;une vie consacr&eacute;e &agrave; la pl&eacute;nitude du Saint Esprit moment apr&egrave;s moment.</p>

<h2>Vivre par la Foi</h2>

<p>Le quatri&egrave;me domaine de la marche par l&rsquo;Esprit est vivre par la foi. Il est malheureux&nbsp; de voir des chr&eacute;tiens sinc&egrave;res qui ont &eacute;t&eacute; tromp&eacute;s par une insistance maladroite sur les &eacute;motions. Quand des espoirs irr&eacute;alistes sont impos&eacute;s par les autres qui ont &eacute;tabli leurs propres standards de preuve pour le Saint Esprit il ne peut rien y avoir plus tard &agrave; part la d&eacute;ception. Gloire soit rendue &agrave; Dieu pour le fait que nous ne vivons pas sur la base des &eacute;motions fluctuantes mais par la foi en Sa Parole qui ne change jamais&nbsp;!&nbsp; Et Sa Parole n&rsquo;est pas silencieuse quant &agrave; la question de la foi. H&eacute;breux 11&nbsp;:6 nous dit que &laquo;&hellip; sans la foi, il est impossible de Lui &ecirc;tre agr&eacute;able&nbsp;&raquo;.&nbsp; Galates 3&nbsp;:11 nous rappelle que nous vivons &laquo;&nbsp;par la foi&nbsp;&raquo;.<br />
<br />
La foi requiert qu&rsquo;on croie alors qu&rsquo;il n&rsquo;est pas facile d&rsquo;agir ainsi. Mais Dieu nous a donn&eacute; une corde de s&eacute;curit&eacute; pour que nous restions fermement attach&eacute;s &agrave; Lui quand les choses sont dures. Romains 8&nbsp;:28 nous promet que &laquo;&nbsp; &hellip; toutes choses concourent au bien de ceux qui aiment Dieu, de ceux qui sont appel&eacute;s selon Son dessein&nbsp;&raquo;.<br />
<br />
Il n&rsquo;est pas facile d&rsquo;apprendre &agrave; dire &laquo;&nbsp;Merci Seigneur&nbsp;&raquo; lorsque votre c&oelig;ur est bris&eacute;, mais le faire est un ajout inestimable &agrave; la marche chr&eacute;tienne<br />
<br />
L&rsquo;Ecrivain Joseph Bayly, qui a perdu trois fils au fil des ans a dit que Dieu n&rsquo;a jamais &eacute;t&eacute; aussi pr&egrave;s d&rsquo;eux que lorsque sa femme et lui rentraient de l&rsquo;enterrement d&rsquo;un de leur fils.<br />
<br />
La louange et les actions de gr&acirc;ce sont des dons qui expriment notre confiance en Dieu au milieu des circonstances embarrassantes. Avez-vous perdu un &ecirc;tre cher? Votre corps semble-t-il &ecirc;tre contr&ocirc;l&eacute; par les douleurs et la maladie? Avez-vous re&ccedil;u une blessure que vous ne m&eacute;ritez pas&nbsp;? Avez-vous subi des pertes financi&egrave;res&nbsp;? Avez-vous essay&eacute; de remercier Dieu&nbsp;bien que rien de tout &ccedil;a n&rsquo;a de sens? Lui avez-vous dit que vous Lui faites confiance bien que la vie soit en train de vous faire porter tout son poids&nbsp;?<br />
<br />
Si nous croyons en Dieu et en Ses promesses, lorsque les choses semblent s&rsquo;effondrer autour de nous, nous reconnaissons Sa seigneurie, et ob&eacute;issons &agrave; son commandement qui est de Lui faire confiance quand nous nous ne pouvons pas voir la fin. Dans I Thessaloniciens 5&nbsp;:18, nous lisons&nbsp;: &laquo;&nbsp;&nbsp;Rendez gr&acirc;ces en toutes choses, car c&#39;est &agrave; votre &eacute;gard la volont&eacute; de Dieu en J&eacute;sus Christ. Il promet des r&eacute;compenses lorsque nous lui faisons confiance. Il a dit que &laquo;&nbsp;Tout&nbsp;&raquo; concourra au bien, et il garde Sa Parole.<br />
<br />
Il peut sembler que seul un insens&eacute; pourrait &ecirc;tre reconnaissant (&agrave; Dieu) en de pareilles circonstances, mais si nous croyons que la Parole de Dieu est vraie, alors nous devons exercer notre volont&eacute; et rendre gr&acirc;ce quand il ne semble y avoir aucune raison&nbsp; pour rendre gr&acirc;ce. Au fil des ans, les chr&eacute;tiens de par le monde ont appris des belles et pr&eacute;cieuses le&ccedil;ons en &eacute;tant simplement ob&eacute;issants &agrave; la Parole de Dieu et en rendant gr&acirc;ce (&agrave; Dieu) <em>quand ils se sentent le moins &agrave; m&ecirc;me de le faire. </em></p>

<h2>Maintenez Christ &agrave; la Direction de votre Vie</h2>

<p>Pour r&eacute;sumer, le chr&eacute;tien voudra marcher par l&rsquo;Esprit moment apr&egrave;s moment parce que Dieu nous a ordonn&eacute; de faire ainsi.&nbsp; C&rsquo;est le seul moyen de maintenir Christ sur le tr&ocirc;ne et au contr&ocirc;le de nos vies. Et, &agrave; mesure que le moi diminue et Christ augmente (Galate 2&nbsp;:20), le r&eacute;sultat sera une croissance incroyable et une vie chr&eacute;tienne abondante.</p>

<h2>Application</h2>

<ol>
	<li>Qu&rsquo;avez-vous aim&eacute; le plus (qu&rsquo;est-ce qui a retenu votre attention)?</li>
	<li>Pourquoi?</li>
	<li>A qui devrais-je transmettre cette information ?</li>
</ol>

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


<p>Adapt&eacute; de Les Messages Transmissibles par Bill Bright. &copy; Cru. Tous droits r&eacute;serv&eacute;s</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Comment marcher par l\'Esprit: ', '/content/M2/fra/tc/ct04.html')">
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