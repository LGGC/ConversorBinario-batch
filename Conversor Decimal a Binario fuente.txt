@echo off
title Decimal a Binario
set /p decimal=Inserte decimal ^>^>^>
cls
echo.Codigo binario de %decimal% :
set bin=2
set "resultado="
set "dectobin="
goto :dectobin
:dectobin
set /a r=%decimal%%%bin%
set /a decimal=%decimal% / %bin%
set resultado=%r%%resultado%
if %decimal% GTR 0 (goto :dectobin)
set dectobin=%resultado%
echo.
echo.%dectobin%
pause
exit