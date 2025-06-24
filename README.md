#modify the -FilePath...


#Program start
########### Starting animation##############

$WriteChar = @('|', ' ', 'S','t','a','r','t','i','n','g', ' ', '|')
$i = 0

for ($i = 0; $i -le $WriteChar.Length*2-2; $i++)
{
  Write-Host " " -NoNewline -ForegroundColor Black -BackgroundColor White
  Write-Host "_" -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 50
} 

Write-Host ""

$j = 0
while ($j -le 1){
  Write-Host $WriteChar -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 100
  $j = $j + 1
}

Write-Host ""
$k = 0

for ($k = 0; $k -le $WriteChar.Length*2-2; $k++)
{
  Write-Host " " -NoNewline -ForegroundColor Black -BackgroundColor White
  Write-Host "_" -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 50
} 
########### end of starting animation #########################

Write-Host ""
########## Closes VS Code #####################

$vscodeProcess = Get-Process -Name "Code" -ErrorAction SilentlyContinue

if ($vscodeProcess){
  Stop-Process -Name "Code" -Force
  Write-Host "Vs Code successfully closed :)" -ForegroundColor white -BackgroundColor Black
}
else{
  Write-Host "Vs Code refused to close! x_x" -ForegroundColor red -BackgroundColor Black
}

######### Reopens VS Code ################
$vscodeProcess = Get-Process -Name "Code" -ErrorAction SilentlyContinue

if (!($vscodeProcess)){
  #modify this FilePath to something else
  Start-Process -FilePath "C:\Users\User\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Visual Studio Code\Visual Studio Code.lnk"
  Write-Host "Vs Code successfully opened :)" -ForegroundColor white -BackgroundColor Black
}
else{
  Write-Host "Vs Code refused to open! x_x" -ForegroundColor red -BackgroundColor Black
}


####### close app ###########
#Program start
$WriteChar = @('|', ' ', 'C','o','m','p','l','e','t','e', ' ', '|')
$i = 0

for ($i = 0; $i -le $WriteChar.Length*2-2; $i++)
{
  Write-Host " " -NoNewline -ForegroundColor Black -BackgroundColor White
  Write-Host "_" -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 50
} 

Write-Host ""

$j = 0
while ($j -le 1){
  Write-Host $WriteChar -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 100
  $j = $j + 1
}

Write-Host ""
$k = 0

for ($k = 0; $k -le $WriteChar.Length*2-2; $k++)
{
  Write-Host " " -NoNewline -ForegroundColor Black -BackgroundColor White
  Write-Host "_" -NoNewline -ForegroundColor Black -BackgroundColor White
  Start-Sleep -Milliseconds 50
}
