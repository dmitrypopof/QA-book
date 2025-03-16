[Назад](README.md)

Условия для явного ожидания `WebDriverWait`

1. Ожидание, пока элемент не станет кликабельным: `wait.until(ExpectedConditions.elementToBeClickable(locator)).click();`
2. Ожидание видимости элемента `wait.until(ExpectedConditions.visibilityOfElementLocated(locator)).click();`
3. Ожидание, что элемент станет невидимым (например, для ожидания исчезновения загрузочного индикатора): `wait.until(ExpectedConditions.invisibilityOfElementLocated(locator));`
4. Ожидание присутствия элемента в DOM: `wait.until(ExpectedConditions.presenceOfElementLocated(locator)).click();`
5. Ожидание, что текст элемента будет изменен на определенное значение: `wait.until(ExpectedConditions.textToBe(locator, "ожидаемый текст"));`
6. Ожидание, что атрибут элемента будет иметь определенное значение: `wait.until(ExpectedConditions.attributeToBe(locator, "атрибут", "значение"));`
