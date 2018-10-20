# alps-touchpad-kext_and_prefpane_to-high-sierra
Kext VoodooPs2 modificada para touchpad alps e painel de preferências 
Testada no notebook Dell Vostro 3460
 
<p>
Para instalação pode utilizar o kext utility e instalar em System/Library/Extensions
</p>

<p>
Após a instalação pode ser que o touchpad não seja reconhecido em Preferências do Sistema,
neste caso é necessário a substituição do arquivo Trackpad.prefPane em System/Library/PreferencePanes
</p>

<p>
Para realizar esta substituição você precisa iniciar por um pendrive de boot pois não terá permissões de escrita no dirtório.
</p>
<p>
Passos recomendados:
</p>

<b>PELO FINDER, AINDA NO SISTEMA INSTALADO</b>
<ul>
  <li>
  1- Faça backup do arquivo Trackpad.prefPane original localizado em System/Library/PreferencePanes
  </li>
  <li>
  2- Copiar o novo arquivo, já extraido, para a raiz do disco.
  </li>
  </ul>
  
<b>PELO PENBOOT</b>
<ul>
  <li>
  3- Iniciar por um penboot e no menu "Utilitários" acessar o terminal.
  </li>
  <li>
  4- remover o arquivo Trackpad.prefPane (lembre do backup no passo 1)
  </li>
  
  > rm -rf System/Library/PreferencePanes/Trackpad.prefPane
  <li>
  5- Copie o novo arquivo para o diretório
  </li>
  
   > cp -R Trackpad.prefPane System/Library/PreferencePanes/
   </ul>
    <p>
 Você pode obter uma mensagem de que "este arquivo é um diretório" para corrigir isso tenha atenção nas barras, 
 cp -R Trackpad.prefPane é diferente de cp -R Trackpad.prefPane/
 
 </p>

