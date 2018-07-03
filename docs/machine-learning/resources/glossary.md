---
title: Glosario de aprendizaje automático
description: Un glosario de términos sobre aprendizaje automático.
author: jralexander
ms.author: johalex
ms.date: 05/31/2018
ms.topic: conceptual
ms.prod: dotnet-ml
ms.devlang: dotnet
manager: wpickett
ms.openlocfilehash: 332d9e14bea165992f9f00b048286e185269ea79
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2018
ms.locfileid: "34860692"
---
# <a name="machine-learning-glossary"></a><span data-ttu-id="bf3f0-103">Glosario de aprendizaje automático</span><span class="sxs-lookup"><span data-stu-id="bf3f0-103">Machine learning glossary</span></span>

<span data-ttu-id="bf3f0-104">La lista siguiente es una compilación de los términos importantes sobre aprendizaje automático que resultan de utilidad al crear los modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-104">The following list is a compilation of important machine learning terms that are useful as you build your custom models.</span></span>

## <a name="accuracy"></a><span data-ttu-id="bf3f0-105">Exactitud</span><span class="sxs-lookup"><span data-stu-id="bf3f0-105">Accuracy</span></span>

<span data-ttu-id="bf3f0-106">En [clasificación](#classification), la exactitud es el número de elementos correctamente clasificados dividido entre el número total de elementos en el conjunto de pruebas.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-106">In [classification](#classification), accuracy is the number of correctly classified items divided by the total number of items in the test set.</span></span> <span data-ttu-id="bf3f0-107">Va desde 0 (el menos preciso) a 1 (el más preciso).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-107">Ranges from 0 (least accurate) to 1 (most accurate).</span></span> <span data-ttu-id="bf3f0-108">La exactitud es una de las métricas de evaluación del rendimiento de su modelo.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-108">Accuracy is one of evaluation metrics of the performance of your model.</span></span> <span data-ttu-id="bf3f0-109">Trátela junto con el valor de [precisión](#precision), el de [recuperación](#recall) y la [puntuación F](#f-score).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-109">Consider it in conjunction with [precision](#precision), [recall](#recall), and [F-score](#f-score).</span></span>

<span data-ttu-id="bf3f0-110">API de ML.NET relacionada: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Accuracy?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-110">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Accuracy?displayProperty=nameWithType>.</span></span>

## <a name="area-under-the-curve-auc"></a><span data-ttu-id="bf3f0-111">Área bajo la curva (AUC)</span><span class="sxs-lookup"><span data-stu-id="bf3f0-111">Area under the curve (AUC)</span></span>

<span data-ttu-id="bf3f0-112">En [clasificación binaria](#binary-classification), una métrica de evaluación que es el valor del área bajo la curva que traza la tasa de verdaderos positivos (en el eje y) en relación con la tasa de falsos positivos (en el eje x).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-112">In [binary classification](#binary-classification), an evaluation metric that is the value of the area under the curve that plots the true positives rate (on the y-axis) against the false positives rate (on the x-axis).</span></span> <span data-ttu-id="bf3f0-113">Va de 0,5 (el peor) a 1 (el mejor).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-113">Ranges from 0.5 (worst) to 1 (best).</span></span> <span data-ttu-id="bf3f0-114">También conocida como el área bajo la curva ROC; es decir, la curva característica operativa del receptor.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-114">Also known as the area under the ROC curve, i.e., receiver operating characteristic curve.</span></span> <span data-ttu-id="bf3f0-115">Para obtener más información, consulte el artículo de Wikipedia [Curva ROC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-115">For more information, see the [Receiver operating characteristic](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) article on Wikipedia.</span></span>

<span data-ttu-id="bf3f0-116">API de ML.NET relacionada:<xref:Microsoft.ML.Models.BinaryClassificationMetrics.Auc?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-116">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.Auc?displayProperty=nameWithType>.</span></span>

## <a name="binary-classification"></a><span data-ttu-id="bf3f0-117">Clasificación binaria</span><span class="sxs-lookup"><span data-stu-id="bf3f0-117">Binary classification</span></span>

<span data-ttu-id="bf3f0-118">Un caso de [clasificación](#classification) donde la [etiqueta](#label) es solo una de dos clases.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-118">A [classification](#classification) case where the [label](#label) is only one out of two classes.</span></span> <span data-ttu-id="bf3f0-119">Para obtener más información, consulte el artículo de Wikipedia [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) (Clasificación binaria).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-119">For more information, see the [Binary classification](https://en.wikipedia.org/wiki/Binary_classification) article on Wikipedia.</span></span>

## <a name="classification"></a><span data-ttu-id="bf3f0-120">Clasificación</span><span class="sxs-lookup"><span data-stu-id="bf3f0-120">Classification</span></span>

<span data-ttu-id="bf3f0-121">Cuando los datos se usan para predecir una categoría, la tarea de [aprendizaje automático supervisado](#supervised-machine-learning) se llama clasificación.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-121">When the data is used to predict a category, [supervised machine learning](#supervised-machine-learning) task is called classification.</span></span> <span data-ttu-id="bf3f0-122">La [clasificación binaria](#binary-classification) hace referencia a la predicción de únicamente dos categorías (por ejemplo, clasificar una imagen como la foto de un "gato" o un "perro").</span><span class="sxs-lookup"><span data-stu-id="bf3f0-122">[Binary classification](#binary-classification) refers to predicting only two categories (for example, classifying an image as a picture of either a 'cat' or a 'dog').</span></span> <span data-ttu-id="bf3f0-123">La [clasificación multiclase ](#multiclass-classification) hace referencia a la predicción de varias categorías (por ejemplo, clasificar una imagen como la foto de una raza específica de perro).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-123">[Multiclass classification](#multiclass-classification) refers to predicting multiple categories (for example, when classifying an image as a picture of a specific breed of dog).</span></span>

## <a name="coefficient-of-determination"></a><span data-ttu-id="bf3f0-124">Coeficiente de determinación</span><span class="sxs-lookup"><span data-stu-id="bf3f0-124">Coefficient of determination</span></span>

<span data-ttu-id="bf3f0-125">En [regresión](#regression), una métrica de evaluación que indica en qué grado los datos se ajustan a un modelo.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-125">In [regression](#regression), an evaluation metric that indicates how well data fits a model.</span></span> <span data-ttu-id="bf3f0-126">Va de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-126">Ranges from 0 to 1.</span></span> <span data-ttu-id="bf3f0-127">Un valor de 0 significa que los datos son aleatorios o no pueden ajustarse al modelo.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-127">A value of 0 means that the data is random or otherwise cannot be fit to the model.</span></span> <span data-ttu-id="bf3f0-128">Un valor de 1 significa que el modelo coincide exactamente con los datos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-128">A value of 1 means that the model exactly matches the data.</span></span> <span data-ttu-id="bf3f0-129">Esto se conoce a menudo como r<sup>2</sup>, R<sup>2</sup>, o r cuadrado.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-129">This is often referred to as r<sup>2</sup>, R<sup>2</sup>, or r-squared.</span></span>

<span data-ttu-id="bf3f0-130">API de ML.NET relacionada: <xref:Microsoft.ML.Models.RegressionMetrics.RSquared?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-130">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.RSquared?displayProperty=nameWithType>.</span></span>

## <a name="feature"></a><span data-ttu-id="bf3f0-131">Característica</span><span class="sxs-lookup"><span data-stu-id="bf3f0-131">Feature</span></span>

<span data-ttu-id="bf3f0-132">Una propiedad medible del fenómeno que se mide, generalmente un valor numérico (doble).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-132">A measurable property of the phenomenon being measured, typically a numeric (double) value.</span></span> <span data-ttu-id="bf3f0-133">Las características múltiples se conocen como **vector de características** y generalmente se almacenan como `double[]`.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-133">Multiple features are referred to as a **Feature vector** and typically stored as `double[]`.</span></span> <span data-ttu-id="bf3f0-134">Las características definen los elementos importantes del fenómeno que se mide.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-134">Features define the important characteristics of the phenomenon being measured.</span></span> <span data-ttu-id="bf3f0-135">Para obtener más información, vea el artículo [Feature](https://en.wikipedia.org/wiki/Feature_(machine_learning)) (Característica) en Wikipedia.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-135">For more information, see the [Feature](https://en.wikipedia.org/wiki/Feature_(machine_learning)) article on Wikipedia.</span></span>

## <a name="feature-engineering"></a><span data-ttu-id="bf3f0-136">Ingeniería de características</span><span class="sxs-lookup"><span data-stu-id="bf3f0-136">Feature engineering</span></span>

<span data-ttu-id="bf3f0-137">La ingeniería de características es el proceso que implica la definición de un conjunto de [características](#feature) y el desarrollo de software que produce vectores de características a partir de los datos de fenómenos disponibles, es decir, la extracción de características.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-137">Feature engineering is the process that involves defining a set of [features](#feature) and developing software that produces feature vectors from available phenomenon data, i.e., feature extraction.</span></span> <span data-ttu-id="bf3f0-138">Para obtener más información, vea el artículo [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering) (Ingeniería de características) en Wikipedia.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-138">For more information, see the [Feature engineering](https://en.wikipedia.org/wiki/Feature_engineering) article on Wikipedia.</span></span>

## <a name="f-score"></a><span data-ttu-id="bf3f0-139">Puntuación F</span><span class="sxs-lookup"><span data-stu-id="bf3f0-139">F-score</span></span>

<span data-ttu-id="bf3f0-140">En [clasificación](#classification), una métrica de evaluación que equilibra [precisión](#precision) y [recuperación](#recall).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-140">In [classification](#classification), an evaluation metric that balances [precision](#precision) and [recall](#recall).</span></span>

<span data-ttu-id="bf3f0-141">API de ML.NET relacionada: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.F1Score?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-141">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.F1Score?displayProperty=nameWithType>.</span></span>

## <a name="hyperparameter"></a><span data-ttu-id="bf3f0-142">Hiperparámetro</span><span class="sxs-lookup"><span data-stu-id="bf3f0-142">Hyperparameter</span></span>

<span data-ttu-id="bf3f0-143">Un parámetro de un algoritmo de aprendizaje automático.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-143">A parameter of a machine learning algorithm.</span></span> <span data-ttu-id="bf3f0-144">Algunos ejemplos son el número de árboles para aprender en un bosque de decisión o el tamaño de paso en un algoritmo de gradiente descendente.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-144">Examples include the number of trees to learn in a decision forest or the step size in a gradient descent algorithm.</span></span> <span data-ttu-id="bf3f0-145">Los valores de los *hiperparámetros* se establecen antes de entrenar el modelo y rigen el proceso de búsqueda de los parámetros de la función de predicción; por ejemplo, los puntos de comparación en un árbol de decisión o las ponderaciones en un modelo de regresión lineal.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-145">Values of *Hyperparameters* are set before training the model and govern the process of finding the parameters of the prediction function, for example, the comparison points in a decision tree or the weights in a linear regression model.</span></span> <span data-ttu-id="bf3f0-146">Para obtener más información, vea el artículo [Hyperparameter](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)) (Hiperparámetro) en Wikipedia.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-146">For more information, see the [Hyperparameter](https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)) article on Wikipedia.</span></span>

## <a name="label"></a><span data-ttu-id="bf3f0-147">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="bf3f0-147">Label</span></span>

<span data-ttu-id="bf3f0-148">El elemento que se va a predecir con el modelo de aprendizaje automático.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-148">The element to be predicted with the machine learning model.</span></span> <span data-ttu-id="bf3f0-149">Por ejemplo, una raza de perro o el precio futuro de unas acciones.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-149">For example, the breed of dog or a future stock price.</span></span>

## <a name="log-loss"></a><span data-ttu-id="bf3f0-150">Pérdida de registro</span><span class="sxs-lookup"><span data-stu-id="bf3f0-150">Log loss</span></span>

<span data-ttu-id="bf3f0-151">En [clasificación](#classification), una métrica de evaluación que caracteriza la precisión de un clasificador.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-151">In [classification](#classification), an evaluation metric that characterizes the accuracy of a classifier.</span></span> <span data-ttu-id="bf3f0-152">Cuanto menor sea la pérdida de registro, más preciso será un clasificador.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-152">The smaller log loss is, the more accurate a classifier is.</span></span>

<span data-ttu-id="bf3f0-153">API de ML.NET relacionada: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.LogLoss?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-153">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.LogLoss?displayProperty=nameWithType>.</span></span>

## <a name="mean-absolute-error-mae"></a><span data-ttu-id="bf3f0-154">Error de media absoluto</span><span class="sxs-lookup"><span data-stu-id="bf3f0-154">Mean absolute error (MAE)</span></span>

<span data-ttu-id="bf3f0-155">En [regresión](#regression), una métrica de evaluación que es el promedio de todos los errores del modelo, donde el error del modelo es la distancia entre el valor de la [etiqueta](#label) predicho y el valor de la etiqueta correcto.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-155">In [regression](#regression), an evaluation metric that is the average of all the model errors, where model error is the distance between the predicted [label](#label) value and the correct label value.</span></span>

<span data-ttu-id="bf3f0-156">API de ML.NET relacionada: <xref:Microsoft.ML.Models.RegressionMetrics.L1?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-156">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.L1?displayProperty=nameWithType>.</span></span>

## <a name="model"></a><span data-ttu-id="bf3f0-157">Modelo</span><span class="sxs-lookup"><span data-stu-id="bf3f0-157">Model</span></span>

<span data-ttu-id="bf3f0-158">Tradicionalmente, los parámetros de la función de predicción.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-158">Traditionally, the parameters for the prediction function.</span></span> <span data-ttu-id="bf3f0-159">Por ejemplo, las ponderaciones en un modelo de regresión lineal o los puntos de división en un árbol de decisión.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-159">For example, the weights in a linear regression model or the split points in a decision tree.</span></span> <span data-ttu-id="bf3f0-160">En ML.NET, un modelo contiene toda la información necesaria para predecir la [etiqueta](#label) de un objeto de dominio (por ejemplo, imagen o texto).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-160">In ML.NET, a model contains all the information necessary to predict the [label](#label) of a domain object (for example, image or text).</span></span> <span data-ttu-id="bf3f0-161">Esto significa que los modelos de ML.NET incluyen los pasos de caracterización necesarios, así como los parámetros para la función de predicción.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-161">This means that ML.NET models include the featurization steps necessary as well as the parameters for the prediction function.</span></span>

## <a name="multiclass-classification"></a><span data-ttu-id="bf3f0-162">Clasificación multiclase</span><span class="sxs-lookup"><span data-stu-id="bf3f0-162">Multiclass classification</span></span>

<span data-ttu-id="bf3f0-163">Un caso de [clasificación](#classification) donde la [etiqueta](#label) es una de tres o más clases.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-163">A [classification](#classification) case where the [label](#label) is one out of three or more classes.</span></span> <span data-ttu-id="bf3f0-164">Para obtener más información, consulte el artículo de Wikipedia [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) (Clasificación multiclase).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-164">For more information, see the [Multiclass classification](https://en.wikipedia.org/wiki/Multiclass_classification) article on Wikipedia.</span></span>

## <a name="n-gram"></a><span data-ttu-id="bf3f0-165">N-grama</span><span class="sxs-lookup"><span data-stu-id="bf3f0-165">N-gram</span></span>

<span data-ttu-id="bf3f0-166">Un esquema de extracción de características para datos de texto: cualquier secuencia de N palabras se convierte en un valor de [característica](#feature).</span><span class="sxs-lookup"><span data-stu-id="bf3f0-166">A feature extraction scheme for text data: any sequence of N words turns into a [feature](#feature) value.</span></span>

## <a name="numerical-feature-vector"></a><span data-ttu-id="bf3f0-167">Vector de características numérico</span><span class="sxs-lookup"><span data-stu-id="bf3f0-167">Numerical feature vector</span></span>

<span data-ttu-id="bf3f0-168">Un vector de [características](#feature) que se compone únicamente de valores numéricos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-168">A [feature](#feature) vector consisting only of numerical values.</span></span> <span data-ttu-id="bf3f0-169">Esto es similar a `double[]`.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-169">This is similar to `double[]`.</span></span>

## <a name="pipeline"></a><span data-ttu-id="bf3f0-170">Canalización</span><span class="sxs-lookup"><span data-stu-id="bf3f0-170">Pipeline</span></span>

<span data-ttu-id="bf3f0-171">Todas las operaciones necesarias para ajustar un modelo a un conjunto de datos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-171">All of the operations needed to fit a model to a data set.</span></span> <span data-ttu-id="bf3f0-172">Una canalización consta de pasos de importación, transformación, caracterización y aprendizaje de datos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-172">A pipeline consists of data import, transformation, featurization, and learning steps.</span></span> <span data-ttu-id="bf3f0-173">Una vez que una canalización está entrenada, se convierte en un modelo.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-173">Once a pipeline is trained, it turns into a model.</span></span>

## <a name="precision"></a><span data-ttu-id="bf3f0-174">Precisión</span><span class="sxs-lookup"><span data-stu-id="bf3f0-174">Precision</span></span>

<span data-ttu-id="bf3f0-175">En [clasificación](#classification), la precisión de una clase es el número de elementos con una predicción correcta en cuando a pertenencia a esa clase dividido entre el número total de elementos cuya predicción señalaba la pertenencia a esa clase.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-175">In [classification](#classification), the precision for a class is the number of items correctly predicted as belonging to that class divided by the total number of items predicted as belonging to the class.</span></span>

<span data-ttu-id="bf3f0-176">API de ML.NET relacionada:<xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativePrecision?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositivePrecision?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-176">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativePrecision?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositivePrecision?displayProperty=nameWithType>.</span></span>

## <a name="recall"></a><span data-ttu-id="bf3f0-177">Recuperación</span><span class="sxs-lookup"><span data-stu-id="bf3f0-177">Recall</span></span>

<span data-ttu-id="bf3f0-178">En [clasificación](#classification), la recuperación de una clase es el número de elementos con una predicción correcta en cuando a pertenencia a esa clase dividido entre el número total de elementos que efectivamente pertenecen a la clase.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-178">In [classification](#classification), the recall for a class is the number of items correctly predicted as belonging to that class divided by the total number of items that actually belong to the class.</span></span>

<span data-ttu-id="bf3f0-179">API de ML.NET relacionada:<xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativeRecall?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositiveRecall?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-179">Related ML.NET API: <xref:Microsoft.ML.Models.BinaryClassificationMetrics.NegativeRecall?displayProperty=nameWithType>, <xref:Microsoft.ML.Models.BinaryClassificationMetrics.PositiveRecall?displayProperty=nameWithType>.</span></span>

## <a name="regression"></a><span data-ttu-id="bf3f0-180">Regresión</span><span class="sxs-lookup"><span data-stu-id="bf3f0-180">Regression</span></span>

<span data-ttu-id="bf3f0-181">Una tarea de [aprendizaje automático supervisada](#supervised-machine-learning) donde el resultado es un valor real, por ejemplo, doble.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-181">A [supervised machine learning](#supervised-machine-learning) task where the output is a real value, for example, double.</span></span> <span data-ttu-id="bf3f0-182">Por ejemplo, la predicción de los precios de las acciones.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-182">Examples include predicting stock prices.</span></span>

## <a name="relative-absolute-error"></a><span data-ttu-id="bf3f0-183">Error absoluto relativo</span><span class="sxs-lookup"><span data-stu-id="bf3f0-183">Relative absolute error</span></span>

<span data-ttu-id="bf3f0-184">En [regresión](#regression), una métrica de evaluación que es la suma de todos los errores absolutos dividida entre la suma de las distancias entre los valores de [etiqueta](#label) correctos y el promedio de todos los valores de etiqueta correctos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-184">In [regression](#regression), an evaluation metric that is the sum of all absolute errors divided by the sum of distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="relative-squared-error"></a><span data-ttu-id="bf3f0-185">Error cuadrático relativo</span><span class="sxs-lookup"><span data-stu-id="bf3f0-185">Relative squared error</span></span>

<span data-ttu-id="bf3f0-186">En [regresión](#regression), una métrica de evaluación que es la suma de todos los errores absolutos cuadráticos dividida entre la suma de las distancias cuadráticas existente entre los valores de [etiqueta](#label) correctos y el promedio de todos los valores de etiqueta correctos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-186">In [regression](#regression), an evaluation metric that is the sum of all squared absolute errors divided by the sum of squared distances between correct [label](#label) values and the average of all correct label values.</span></span>

## <a name="root-of-mean-squared-error-rmse"></a><span data-ttu-id="bf3f0-187">Raíz cuadrada del error cuadrático medio</span><span class="sxs-lookup"><span data-stu-id="bf3f0-187">Root of mean squared error (RMSE)</span></span>

<span data-ttu-id="bf3f0-188">En [regresión](#regression), una métrica de evaluación que es la raíz cuadrada del promedio de los cuadrados de los errores.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-188">In [regression](#regression), an evaluation metric that is the square root of the average of the squares of the errors.</span></span>

<span data-ttu-id="bf3f0-189">API de ML.NET relacionada: <xref:Microsoft.ML.Models.RegressionMetrics.Rms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-189">Related ML.NET API: <xref:Microsoft.ML.Models.RegressionMetrics.Rms?displayProperty=nameWithType>.</span></span>

## <a name="supervised-machine-learning"></a><span data-ttu-id="bf3f0-190">Aprendizaje automático supervisado</span><span class="sxs-lookup"><span data-stu-id="bf3f0-190">Supervised machine learning</span></span>

<span data-ttu-id="bf3f0-191">Una subclase de aprendizaje automático en la que un modelo deseado predice la etiqueta de datos aún no vistos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-191">A subclass of machine learning in which a desired model predicts the label for yet-unseen data.</span></span> <span data-ttu-id="bf3f0-192">Algunos ejemplos son la clasificación, la regresión y la predicción estructurada.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-192">Examples include classification, regression, and structured prediction.</span></span> <span data-ttu-id="bf3f0-193">Para obtener más información, vea el artículo [Aprendizaje supervisado](https://en.wikipedia.org/wiki/Supervised_learning) en Wikipedia.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-193">For more information, see the  [Supervised learning](https://en.wikipedia.org/wiki/Supervised_learning) article on Wikipedia.</span></span>

## <a name="training"></a><span data-ttu-id="bf3f0-194">Aprendizaje</span><span class="sxs-lookup"><span data-stu-id="bf3f0-194">Training</span></span>

<span data-ttu-id="bf3f0-195">El proceso de identificación de un [modelo](#model) para un conjunto de datos de entrenamiento determinado.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-195">The process of identifying a [model](#model) for a given training data set.</span></span> <span data-ttu-id="bf3f0-196">Para un modelo lineal, esto significa buscar las ponderaciones.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-196">For a linear model, this means finding the weights.</span></span> <span data-ttu-id="bf3f0-197">Para un árbol, implica la identificación de los puntos de división.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-197">For a tree, it involves the identifying the split points.</span></span>

## <a name="transform"></a><span data-ttu-id="bf3f0-198">Transformación</span><span class="sxs-lookup"><span data-stu-id="bf3f0-198">Transform</span></span>

<span data-ttu-id="bf3f0-199">Un componente de [canalización](#pipeline) que transforma los datos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-199">A [pipeline](#pipeline) component that transforms data.</span></span> <span data-ttu-id="bf3f0-200">Por ejemplo, de texto a vector de números.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-200">For example, from text to vector of numbers.</span></span>

## <a name="unsupervised-machine-learning"></a><span data-ttu-id="bf3f0-201">Aprendizaje automático no supervisado</span><span class="sxs-lookup"><span data-stu-id="bf3f0-201">Unsupervised machine learning</span></span>

<span data-ttu-id="bf3f0-202">Una subclase de aprendizaje automático en la que un modelo deseado encuentra una estructura oculta (o latente) en los datos.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-202">A subclass of machine learning in which a desired model finds hidden (or latent) structure in data.</span></span> <span data-ttu-id="bf3f0-203">Algunos ejemplos son la agrupación en clústeres, el modelado de temas y la reducción de la dimensionalidad.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-203">Examples include clustering, topic modeling, and dimensionality reduction.</span></span> <span data-ttu-id="bf3f0-204">Para obtener más información, vea el artículo [Aprendizaje no supervisado](https://en.wikipedia.org/wiki/Unsupervised_learning) en Wikipedia.</span><span class="sxs-lookup"><span data-stu-id="bf3f0-204">For more information, see the [Unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning) article on Wikipedia.</span></span>