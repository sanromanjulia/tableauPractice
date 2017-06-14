# tableauPractice
function initializeViz() {
  var placeholderDiv = document.getElementById("tableauViz");
  var url = "https://catalog.data.gov/dataset/births-to-unmarried-women-by-maternal-age-united-states-1940-2013";
  var options = {
    width: placeholderDiv.offsetWidth,
    height: placeholderDiv.offsetHeight,
    hideTabs: true,
    hideToolbar: true,
    onFirstInteractive: function () {
      workbook = viz.getWorkbook();
      activeSheet = workbook.getActiveSheet();
    }
  };
  viz = new tableau.Viz(placeholderDiv, url, options);
}      
