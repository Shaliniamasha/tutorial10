# tutorial10

# 01

object TemperatureConverter extends App {
  def calculateAverage(temperatures: List[Double]): Double = {
    val fahrenheitTemps = temperatures.map(celsius => (celsius * 9/5) + 32)
    val totalFahrenheit = fahrenheitTemps.reduce(_ + _)
    val averageFahrenheit = totalFahrenheit / temperatures.length.toDouble 
    averageFahrenheit
  }

  val temperatures = List(0.0, 10.0, 20.0, 30.0)
  val averageFahrenheit = calculateAverage(temperatures)
  println(s"Average Fahrenheit temperature: $averageFahrenheit")
}

# 02 

object LetterCounter extends App {
  def countLetterOccurrences(words: List[String]): Int = {
    val letterCounts = words.map(_.length)
    val totalLetterOccurrences = letterCounts.reduce(_ + _)
    totalLetterOccurrences
  }

  val words = List("apple", "banana", "cherry", "date")
  val totalOccurrences = countLetterOccurrences(words)
  println(s"Total count of letter occurrences: $totalOccurrences")
}
