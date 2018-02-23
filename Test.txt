

object Test {
  def main(args: Array[String]): Unit = {  
  /** 
    * 九九乘法表 
    */  
  val tabulate: Array[Array[String]] = Array.tabulate(9, 9) {  
    (i, j) =>  
      val str: String = s"${i + 1}*${j + 1}=${(i + 1) * (j + 1)}"  
      if (j == 0) str else f"$str%8s"  
  }  
  tabulate.map(_.mkString).foreach(println)  
}  
}